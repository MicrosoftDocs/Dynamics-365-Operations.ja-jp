---
title: FormContainerControl クラス
description: このトピックでは、FormContainerControl クラスについて説明します。
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
ms.openlocfilehash: 456d2eab0576f6dfdc94cba489851c97f49db519
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502636"
---
# <a name="class-formcontainercontrol"></a><span data-ttu-id="c6648-103">クラス FormContainerControl</span><span class="sxs-lookup"><span data-stu-id="c6648-103">Class FormContainerControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormContainerControl extends FormControl
```

## <a name="remarks"></a><span data-ttu-id="c6648-104">備考</span><span class="sxs-lookup"><span data-stu-id="c6648-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c6648-105">例</span><span class="sxs-lookup"><span data-stu-id="c6648-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c6648-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c6648-106">Methods</span></span>

| <span data-ttu-id="c6648-107">方法</span><span class="sxs-lookup"><span data-stu-id="c6648-107">Method</span></span>                                                                                                              | <span data-ttu-id="c6648-108">説明</span><span class="sxs-lookup"><span data-stu-id="c6648-108">Description</span></span> |
|---------------------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="c6648-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="c6648-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |             |
| <span data-ttu-id="c6648-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="c6648-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |             |
| <span data-ttu-id="c6648-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="c6648-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |             |
| <span data-ttu-id="c6648-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |             |
| <span data-ttu-id="c6648-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |             |
| <span data-ttu-id="c6648-114">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-114">public boolean alignControl(\[boolean value\])</span></span>                                                                      |             |
| <span data-ttu-id="c6648-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                         |             |
| <span data-ttu-id="c6648-116">public boolean allowSysSetup()</span><span class="sxs-lookup"><span data-stu-id="c6648-116">public boolean allowSysSetup()</span></span>                                                                                      |             |
| <span data-ttu-id="c6648-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-117">public int allowUserSetup(\[int value\])</span></span>                                                                            |             |
| <span data-ttu-id="c6648-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-118">public int arrangeGuide(\[int value\])</span></span>                                                                              |             |
| <span data-ttu-id="c6648-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-119">public int arrangeMethod(\[int value\])</span></span>                                                                             |             |
| <span data-ttu-id="c6648-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-120">public int arrangeWhen(\[int value\])</span></span>                                                                               |             |
| <span data-ttu-id="c6648-121">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-121">public boolean autoDataGroup(\[boolean value\])</span></span>                                                                     |             |
| <span data-ttu-id="c6648-122">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-122">public boolean autoDeclaration(\[boolean value\])</span></span>                                                                   |             |
| <span data-ttu-id="c6648-123">public int beginDrag(int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c6648-123">public int beginDrag(int x, int y)</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-124">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-124">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |             |
| <span data-ttu-id="c6648-125">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-125">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |             |
| <span data-ttu-id="c6648-126">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-126">public int bottomMarginValue(\[int value\])</span></span>                                                                         |             |
| <span data-ttu-id="c6648-127">public container calcControlSize(int chars, int lines)</span><span class="sxs-lookup"><span data-stu-id="c6648-127">public container calcControlSize(int chars, int lines)</span></span>                                                              |             |
| <span data-ttu-id="c6648-128">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="c6648-128">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |             |
| <span data-ttu-id="c6648-129">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="c6648-129">public boolean canContain(FormControl control)</span></span>                                                                      |             |
| <span data-ttu-id="c6648-130">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-130">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |             |
| <span data-ttu-id="c6648-131">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-131">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |             |
| <span data-ttu-id="c6648-132">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-132">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |             |
| <span data-ttu-id="c6648-133">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-133">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |             |
| <span data-ttu-id="c6648-134">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-134">public int columnspaceValue(\[int value\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-135">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-135">public int columnsValue(\[int value\])</span></span>                                                                              |             |
| <span data-ttu-id="c6648-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-136">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                            |             |
| <span data-ttu-id="c6648-137">public List configurationKeyEx()</span><span class="sxs-lookup"><span data-stu-id="c6648-137">public List configurationKeyEx()</span></span>                                                                                    |             |
| <span data-ttu-id="c6648-138">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="c6648-138">public boolean contains(FormControl control)</span></span>                                                                        |             |
| <span data-ttu-id="c6648-139">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="c6648-139">public int controlCount()</span></span>                                                                                           |             |
| <span data-ttu-id="c6648-140">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="c6648-140">public FormControl controlNum(int controlNo)</span></span>                                                                        |             |
| <span data-ttu-id="c6648-141">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-141">public str countryRegionCodes(\[str value\])</span></span>                                                                        |             |
| <span data-ttu-id="c6648-142">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-142">public str dataRelationPath(\[str value\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-143">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-143">public int displayTarget(\[int value\])</span></span>                                                                             |             |
| <span data-ttu-id="c6648-144">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-144">public int dragDrop(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c6648-145">public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                   |             |
| <span data-ttu-id="c6648-146">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c6648-146">public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                       |             |
| <span data-ttu-id="c6648-147">public str dragText()</span><span class="sxs-lookup"><span data-stu-id="c6648-147">public str dragText()</span></span>                                                                                               |             |
| <span data-ttu-id="c6648-148">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-148">public boolean enabled(\[boolean value\])</span></span>                                                                           |             |
| <span data-ttu-id="c6648-149">public boolean hasChanged(\[boolean val\])</span><span class="sxs-lookup"><span data-stu-id="c6648-149">public boolean hasChanged(\[boolean val\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-150">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c6648-150">public boolean hasUserSetting()</span></span>                                                                                     |             |
| <span data-ttu-id="c6648-151">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-151">public int height(int value, \[int mode\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-152">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-152">public int heightMode(\[int value\])</span></span>                                                                                |             |
| <span data-ttu-id="c6648-153">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-153">public int heightValue(\[int value\])</span></span>                                                                               |             |
| <span data-ttu-id="c6648-154">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="c6648-154">public str helpField()</span></span>                                                                                              |             |
| <span data-ttu-id="c6648-155">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-155">public str helpText(\[str value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-156">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-156">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |             |
| <span data-ttu-id="c6648-157">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-157">public str hierarchyParent(\[str value\])</span></span>                                                                           |             |
| <span data-ttu-id="c6648-158">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="c6648-158">public int hWnd()</span></span>                                                                                                   |             |
| <span data-ttu-id="c6648-159">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="c6648-159">public boolean isContainer()</span></span>                                                                                        |             |
| <span data-ttu-id="c6648-160">public boolean isDisplayed()</span><span class="sxs-lookup"><span data-stu-id="c6648-160">public boolean isDisplayed()</span></span>                                                                                        |             |
| <span data-ttu-id="c6648-161">public boolean isRestricted()</span><span class="sxs-lookup"><span data-stu-id="c6648-161">public boolean isRestricted()</span></span>                                                                                       |             |
| <span data-ttu-id="c6648-162">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="c6648-162">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            |             |
| <span data-ttu-id="c6648-163">public boolean isVisible()</span><span class="sxs-lookup"><span data-stu-id="c6648-163">public boolean isVisible()</span></span>                                                                                          |             |
| <span data-ttu-id="c6648-164">public boolean isVisibleOnClient()</span><span class="sxs-lookup"><span data-stu-id="c6648-164">public boolean isVisibleOnClient()</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-165">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-165">public int left(int value, \[int mode\])</span></span>                                                                            |             |
| <span data-ttu-id="c6648-166">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-166">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |             |
| <span data-ttu-id="c6648-167">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-167">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |             |
| <span data-ttu-id="c6648-168">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-168">public int leftMarginValue(\[int value\])</span></span>                                                                           |             |
| <span data-ttu-id="c6648-169">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-169">public int leftMode(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-170">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-170">public int leftValue(\[int value\])</span></span>                                                                                 |             |
| <span data-ttu-id="c6648-171">public boolean markAsUserAdd(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-171">public boolean markAsUserAdd(\[boolean value\])</span></span>                                                                     |             |
| <span data-ttu-id="c6648-172">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c6648-172">public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                     |             |
| <span data-ttu-id="c6648-173">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c6648-173">public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         |             |
| <span data-ttu-id="c6648-174">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c6648-174">public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                         |             |
| <span data-ttu-id="c6648-175">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c6648-175">public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                           |             |
| <span data-ttu-id="c6648-176">public int moveControl(int controlId, \[int insertAfterId\])</span><span class="sxs-lookup"><span data-stu-id="c6648-176">public int moveControl(int controlId, \[int insertAfterId\])</span></span>                                                        |             |
| <span data-ttu-id="c6648-177">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-177">public str name(\[str value\])</span></span>                                                                                      |             |
| <span data-ttu-id="c6648-178">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-178">public int neededPermission(\[int value\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-179">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="c6648-179">public container SysObsoleteAttribute()</span></span>                                                                             |             |
| <span data-ttu-id="c6648-180">public FormControl parentControl()</span><span class="sxs-lookup"><span data-stu-id="c6648-180">public FormControl parentControl()</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-181">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-181">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |             |
| <span data-ttu-id="c6648-182">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-182">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |             |
| <span data-ttu-id="c6648-183">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-183">public int rightMarginValue(\[int value\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-184">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-184">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                           |             |
| <span data-ttu-id="c6648-185">public int showContextMenu(int menuHandle)</span><span class="sxs-lookup"><span data-stu-id="c6648-185">public int showContextMenu(int menuHandle)</span></span>                                                                          |             |
| <span data-ttu-id="c6648-186">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-186">public boolean skip(\[boolean value\])</span></span>                                                                              |             |
| <span data-ttu-id="c6648-187">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="c6648-187">public str toolTip()</span></span>                                                                                                |             |
| <span data-ttu-id="c6648-188">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-188">public int top(int value, \[int mode\])</span></span>                                                                             |             |
| <span data-ttu-id="c6648-189">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-189">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |             |
| <span data-ttu-id="c6648-190">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-190">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |             |
| <span data-ttu-id="c6648-191">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-191">public int topMarginValue(\[int value\])</span></span>                                                                            |             |
| <span data-ttu-id="c6648-192">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-192">public int topMode(\[int value\])</span></span>                                                                                   |             |
| <span data-ttu-id="c6648-193">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-193">public int topValue(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-194">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-194">public int type(\[int value\])</span></span>                                                                                      |             |
| <span data-ttu-id="c6648-195">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="c6648-195">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |             |
| <span data-ttu-id="c6648-196">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-196">public int userData(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-197">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-197">public int userDataItem(\[int value\])</span></span>                                                                              |             |
| <span data-ttu-id="c6648-198">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-198">public int userDataItems(\[int value\])</span></span>                                                                             |             |
| <span data-ttu-id="c6648-199">public int userDisable(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-199">public int userDisable(\[int value\])</span></span>                                                                               |             |
| <span data-ttu-id="c6648-200">public int userHeight(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-200">public int userHeight(\[int value\])</span></span>                                                                                |             |
| <span data-ttu-id="c6648-201">public int userHide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-201">public int userHide(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-202">public int userOrgContainer(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-202">public int userOrgContainer(\[int value\])</span></span>                                                                          |             |
| <span data-ttu-id="c6648-203">public int userOrgSibling(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-203">public int userOrgSibling(\[int value\])</span></span>                                                                            |             |
| <span data-ttu-id="c6648-204">public str userPromptText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-204">public str userPromptText(\[str value\])</span></span>                                                                            |             |
| <span data-ttu-id="c6648-205">public int userSecurityLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-205">public int userSecurityLevel(\[int value\])</span></span>                                                                         |             |
| <span data-ttu-id="c6648-206">public int userSkip(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-206">public int userSkip(\[int value\])</span></span>                                                                                  |             |
| <span data-ttu-id="c6648-207">public int userWidth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-207">public int userWidth(\[int value\])</span></span>                                                                                 |             |
| <span data-ttu-id="c6648-208">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-208">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |             |
| <span data-ttu-id="c6648-209">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-209">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                        |             |
| <span data-ttu-id="c6648-210">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-210">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                              |             |
| <span data-ttu-id="c6648-211">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-211">public int verticalSpacingValue(\[int value\])</span></span>                                                                      |             |
| <span data-ttu-id="c6648-212">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-212">public boolean visible(\[boolean value\])</span></span>                                                                           |             |
| <span data-ttu-id="c6648-213">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="c6648-213">public int width(int value, \[int mode\])</span></span>                                                                           |             |
| <span data-ttu-id="c6648-214">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-214">public int widthMode(\[int value\])</span></span>                                                                                 |             |
| <span data-ttu-id="c6648-215">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c6648-215">public int widthValue(\[int value\])</span></span>                                                                                |             |
| <span data-ttu-id="c6648-216">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c6648-216">public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)</span></span>                                               |             |
| <span data-ttu-id="c6648-217">public void inputSearch(str searchStr)</span><span class="sxs-lookup"><span data-stu-id="c6648-217">public void inputSearch(str searchStr)</span></span>                                                                              |             |
| <span data-ttu-id="c6648-218">public void prefColumnSize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="c6648-218">public void prefColumnSize(int width, int height)</span></span>                                                                   |             |
| <span data-ttu-id="c6648-219">public void gotFocus()</span><span class="sxs-lookup"><span data-stu-id="c6648-219">public void gotFocus()</span></span>                                                                                              |             |
| <span data-ttu-id="c6648-220">public void lostFocus()</span><span class="sxs-lookup"><span data-stu-id="c6648-220">public void lostFocus()</span></span>                                                                                             |             |
| <span data-ttu-id="c6648-221">public void mouseLeave()</span><span class="sxs-lookup"><span data-stu-id="c6648-221">public void mouseLeave()</span></span>                                                                                            |             |
| <span data-ttu-id="c6648-222">public void setFocus()</span><span class="sxs-lookup"><span data-stu-id="c6648-222">public void setFocus()</span></span>                                                                                              |             |
| <span data-ttu-id="c6648-223">public void copy()</span><span class="sxs-lookup"><span data-stu-id="c6648-223">public void copy()</span></span>                                                                                                  |             |
| <span data-ttu-id="c6648-224">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="c6648-224">private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                         |             |
| <span data-ttu-id="c6648-225">public void displayControl()</span><span class="sxs-lookup"><span data-stu-id="c6648-225">public void displayControl()</span></span>                                                                                        |             |
| <span data-ttu-id="c6648-226">public void paste()</span><span class="sxs-lookup"><span data-stu-id="c6648-226">public void paste()</span></span>                                                                                                 |             |
| <span data-ttu-id="c6648-227">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span><span class="sxs-lookup"><span data-stu-id="c6648-227">public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)</span></span>                                           |             |
| <span data-ttu-id="c6648-228">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="c6648-228">private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])</span></span>                                        |             |
| <span data-ttu-id="c6648-229">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span><span class="sxs-lookup"><span data-stu-id="c6648-229">public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)</span></span>                                       |             |
| <span data-ttu-id="c6648-230">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="c6648-230">public void resetUserSetting()</span></span>                                                                                      |             |
| <span data-ttu-id="c6648-231">public void endDrag()</span><span class="sxs-lookup"><span data-stu-id="c6648-231">public void endDrag()</span></span>                                                                                               |             |
| <span data-ttu-id="c6648-232">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="c6648-232">public void arrange()</span></span>                                                                                               |             |
| <span data-ttu-id="c6648-233">public void dragLeave()</span><span class="sxs-lookup"><span data-stu-id="c6648-233">public void dragLeave()</span></span>                                                                                             |             |
| <span data-ttu-id="c6648-234">public void cut()</span><span class="sxs-lookup"><span data-stu-id="c6648-234">public void cut()</span></span>                                                                                                   |             |
| <span data-ttu-id="c6648-235">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="c6648-235">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span>         |             |
| <span data-ttu-id="c6648-236">public void context()</span><span class="sxs-lookup"><span data-stu-id="c6648-236">public void context()</span></span>                                                                                               |             |

## <a name="method-addcontrol"></a><span data-ttu-id="c6648-237">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="c6648-237">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="c6648-238">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="c6648-238">Parameters - addControl</span></span>

<span data-ttu-id="c6648-239">controlType</span><span class="sxs-lookup"><span data-stu-id="c6648-239">controlType</span></span>  

<!-- -->

<span data-ttu-id="c6648-240">controlName</span><span class="sxs-lookup"><span data-stu-id="c6648-240">controlName</span></span>  

<!-- -->

<span data-ttu-id="c6648-241">insertAfter</span><span class="sxs-lookup"><span data-stu-id="c6648-241">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="c6648-242">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="c6648-242">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="c6648-243">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="c6648-243">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="c6648-244">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="c6648-244">Parameters - addControlEx</span></span>

<span data-ttu-id="c6648-245">controlClass</span><span class="sxs-lookup"><span data-stu-id="c6648-245">controlClass</span></span>  

<!-- -->

<span data-ttu-id="c6648-246">controlName</span><span class="sxs-lookup"><span data-stu-id="c6648-246">controlName</span></span>  

<!-- -->

<span data-ttu-id="c6648-247">insertAfter</span><span class="sxs-lookup"><span data-stu-id="c6648-247">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="c6648-248">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="c6648-248">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="c6648-249">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-249">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="c6648-250">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-250">Parameters - addDataField</span></span>

<span data-ttu-id="c6648-251">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="c6648-251">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="c6648-252">fieldId</span><span class="sxs-lookup"><span data-stu-id="c6648-252">fieldId</span></span>  

<!-- -->

<span data-ttu-id="c6648-253">insertAfter</span><span class="sxs-lookup"><span data-stu-id="c6648-253">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="c6648-254">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="c6648-254">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="c6648-255">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-255">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="c6648-256">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="c6648-256">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="c6648-257">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="c6648-257">Parameters - alignChild</span></span>

<span data-ttu-id="c6648-258">値</span><span class="sxs-lookup"><span data-stu-id="c6648-258">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="c6648-259">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="c6648-259">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="c6648-260">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="c6648-260">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="c6648-261">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="c6648-261">Parameters - alignChildren</span></span>

<span data-ttu-id="c6648-262">値</span><span class="sxs-lookup"><span data-stu-id="c6648-262">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="c6648-263">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="c6648-263">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="c6648-264">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="c6648-264">Method alignControl</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="c6648-265">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="c6648-265">Parameters - alignControl</span></span>

<span data-ttu-id="c6648-266">値</span><span class="sxs-lookup"><span data-stu-id="c6648-266">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="c6648-267">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="c6648-267">Return Value - alignControl</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="c6648-268">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="c6648-268">Method allowEdit</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="c6648-269">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c6648-269">Parameters - allowEdit</span></span>

<span data-ttu-id="c6648-270">値</span><span class="sxs-lookup"><span data-stu-id="c6648-270">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="c6648-271">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="c6648-271">Return Value - allowEdit</span></span>

## <a name="method-allowsyssetup"></a><span data-ttu-id="c6648-272">メソッド allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="c6648-272">Method allowSysSetup</span></span>

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a><span data-ttu-id="c6648-273">戻り値 - allowSysSetup</span><span class="sxs-lookup"><span data-stu-id="c6648-273">Return Value - allowSysSetup</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="c6648-274">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="c6648-274">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="c6648-275">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="c6648-275">Parameters - allowUserSetup</span></span>

<span data-ttu-id="c6648-276">値</span><span class="sxs-lookup"><span data-stu-id="c6648-276">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="c6648-277">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="c6648-277">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="c6648-278">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="c6648-278">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="c6648-279">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="c6648-279">Parameters - arrangeGuide</span></span>

<span data-ttu-id="c6648-280">値</span><span class="sxs-lookup"><span data-stu-id="c6648-280">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="c6648-281">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="c6648-281">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="c6648-282">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="c6648-282">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="c6648-283">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="c6648-283">Parameters - arrangeMethod</span></span>

<span data-ttu-id="c6648-284">値</span><span class="sxs-lookup"><span data-stu-id="c6648-284">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="c6648-285">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="c6648-285">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="c6648-286">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="c6648-286">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="c6648-287">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="c6648-287">Parameters - arrangeWhen</span></span>

<span data-ttu-id="c6648-288">値</span><span class="sxs-lookup"><span data-stu-id="c6648-288">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="c6648-289">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="c6648-289">Return Value - arrangeWhen</span></span>

## <a name="method-autodatagroup"></a><span data-ttu-id="c6648-290">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="c6648-290">Method autoDataGroup</span></span>

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a><span data-ttu-id="c6648-291">パラメーター - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="c6648-291">Parameters - autoDataGroup</span></span>

<span data-ttu-id="c6648-292">値</span><span class="sxs-lookup"><span data-stu-id="c6648-292">value</span></span>  

### <a name="return-value---autodatagroup"></a><span data-ttu-id="c6648-293">戻り値 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="c6648-293">Return Value - autoDataGroup</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="c6648-294">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c6648-294">Method autoDeclaration</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="c6648-295">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c6648-295">Parameters - autoDeclaration</span></span>

<span data-ttu-id="c6648-296">値</span><span class="sxs-lookup"><span data-stu-id="c6648-296">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="c6648-297">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="c6648-297">Return Value - autoDeclaration</span></span>

## <a name="method-begindrag"></a><span data-ttu-id="c6648-298">メソッド beginDrag</span><span class="sxs-lookup"><span data-stu-id="c6648-298">Method beginDrag</span></span>

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a><span data-ttu-id="c6648-299">パラメーター - beginDrag</span><span class="sxs-lookup"><span data-stu-id="c6648-299">Parameters - beginDrag</span></span>

<span data-ttu-id="c6648-300">x</span><span class="sxs-lookup"><span data-stu-id="c6648-300">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-301">y</span><span class="sxs-lookup"><span data-stu-id="c6648-301">y</span></span>  

### <a name="return-value---begindrag"></a><span data-ttu-id="c6648-302">戻り値 - beginDrag</span><span class="sxs-lookup"><span data-stu-id="c6648-302">Return Value - beginDrag</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="c6648-303">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-303">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="c6648-304">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-304">Parameters - bottomMargin</span></span>

<span data-ttu-id="c6648-305">値</span><span class="sxs-lookup"><span data-stu-id="c6648-305">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-306">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-306">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="c6648-307">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-307">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="c6648-308">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-308">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="c6648-309">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-309">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="c6648-310">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-310">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="c6648-311">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-311">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="c6648-312">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-312">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="c6648-313">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-313">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="c6648-314">値</span><span class="sxs-lookup"><span data-stu-id="c6648-314">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="c6648-315">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-315">Return Value - bottomMarginValue</span></span>

## <a name="method-calccontrolsize"></a><span data-ttu-id="c6648-316">メソッド calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c6648-316">Method calcControlSize</span></span>

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a><span data-ttu-id="c6648-317">パラメーター - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c6648-317">Parameters - calcControlSize</span></span>

<span data-ttu-id="c6648-318">chars</span><span class="sxs-lookup"><span data-stu-id="c6648-318">chars</span></span>  

<!-- -->

<span data-ttu-id="c6648-319">明細行</span><span class="sxs-lookup"><span data-stu-id="c6648-319">lines</span></span>  

### <a name="return-value---calccontrolsize"></a><span data-ttu-id="c6648-320">戻り値 - calcControlSize</span><span class="sxs-lookup"><span data-stu-id="c6648-320">Return Value - calcControlSize</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="c6648-321">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-321">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="c6648-322">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-322">Parameters - canAddDataField</span></span>

<span data-ttu-id="c6648-323">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="c6648-323">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="c6648-324">fieldId</span><span class="sxs-lookup"><span data-stu-id="c6648-324">fieldId</span></span>  

<!-- -->

<span data-ttu-id="c6648-325">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="c6648-325">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="c6648-326">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="c6648-326">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="c6648-327">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="c6648-327">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="c6648-328">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="c6648-328">Parameters - canContain</span></span>

<span data-ttu-id="c6648-329">control</span><span class="sxs-lookup"><span data-stu-id="c6648-329">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="c6648-330">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="c6648-330">Return Value - canContain</span></span>

## <a name="method-columns"></a><span data-ttu-id="c6648-331">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="c6648-331">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="c6648-332">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="c6648-332">Parameters - columns</span></span>

<span data-ttu-id="c6648-333">値</span><span class="sxs-lookup"><span data-stu-id="c6648-333">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-334">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-334">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="c6648-335">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="c6648-335">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="c6648-336">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="c6648-336">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="c6648-337">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="c6648-337">Parameters - columnsMode</span></span>

<span data-ttu-id="c6648-338">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-338">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="c6648-339">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="c6648-339">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="c6648-340">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="c6648-340">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="c6648-341">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="c6648-341">Parameters - columnspace</span></span>

<span data-ttu-id="c6648-342">値</span><span class="sxs-lookup"><span data-stu-id="c6648-342">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-343">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-343">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="c6648-344">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="c6648-344">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="c6648-345">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="c6648-345">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="c6648-346">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="c6648-346">Parameters - columnspaceMode</span></span>

<span data-ttu-id="c6648-347">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-347">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="c6648-348">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="c6648-348">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="c6648-349">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="c6648-349">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="c6648-350">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="c6648-350">Parameters - columnspaceValue</span></span>

<span data-ttu-id="c6648-351">値</span><span class="sxs-lookup"><span data-stu-id="c6648-351">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="c6648-352">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="c6648-352">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="c6648-353">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="c6648-353">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="c6648-354">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="c6648-354">Parameters - columnsValue</span></span>

<span data-ttu-id="c6648-355">値</span><span class="sxs-lookup"><span data-stu-id="c6648-355">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="c6648-356">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="c6648-356">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="c6648-357">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="c6648-357">Method configurationKey</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="c6648-358">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c6648-358">Parameters - configurationKey</span></span>

<span data-ttu-id="c6648-359">値</span><span class="sxs-lookup"><span data-stu-id="c6648-359">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="c6648-360">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="c6648-360">Return Value - configurationKey</span></span>

## <a name="method-configurationkeyex"></a><span data-ttu-id="c6648-361">メソッド configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="c6648-361">Method configurationKeyEx</span></span>

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a><span data-ttu-id="c6648-362">戻り値 - configurationKeyEx</span><span class="sxs-lookup"><span data-stu-id="c6648-362">Return Value - configurationKeyEx</span></span>

## <a name="method-contains"></a><span data-ttu-id="c6648-363">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="c6648-363">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="c6648-364">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="c6648-364">Parameters - contains</span></span>

<span data-ttu-id="c6648-365">control</span><span class="sxs-lookup"><span data-stu-id="c6648-365">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="c6648-366">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="c6648-366">Return Value - contains</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="c6648-367">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="c6648-367">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="c6648-368">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="c6648-368">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="c6648-369">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="c6648-369">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="c6648-370">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="c6648-370">Parameters - controlNum</span></span>

<span data-ttu-id="c6648-371">controlNo</span><span class="sxs-lookup"><span data-stu-id="c6648-371">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="c6648-372">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="c6648-372">Return Value - controlNum</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="c6648-373">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c6648-373">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="c6648-374">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c6648-374">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="c6648-375">値</span><span class="sxs-lookup"><span data-stu-id="c6648-375">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="c6648-376">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="c6648-376">Return Value - countryRegionCodes</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="c6648-377">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c6648-377">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="c6648-378">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c6648-378">Parameters - dataRelationPath</span></span>

<span data-ttu-id="c6648-379">値</span><span class="sxs-lookup"><span data-stu-id="c6648-379">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="c6648-380">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="c6648-380">Return Value - dataRelationPath</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="c6648-381">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="c6648-381">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="c6648-382">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="c6648-382">Parameters - displayTarget</span></span>

<span data-ttu-id="c6648-383">値</span><span class="sxs-lookup"><span data-stu-id="c6648-383">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="c6648-384">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="c6648-384">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="c6648-385">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="c6648-385">Method dragDrop</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="c6648-386">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="c6648-386">Parameters - dragDrop</span></span>

<span data-ttu-id="c6648-387">値</span><span class="sxs-lookup"><span data-stu-id="c6648-387">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="c6648-388">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="c6648-388">Return Value - dragDrop</span></span>

## <a name="method-dragover"></a><span data-ttu-id="c6648-389">メソッド dragOver</span><span class="sxs-lookup"><span data-stu-id="c6648-389">Method dragOver</span></span>

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a><span data-ttu-id="c6648-390">パラメーター - dragOver</span><span class="sxs-lookup"><span data-stu-id="c6648-390">Parameters - dragOver</span></span>

<span data-ttu-id="c6648-391">dragSource</span><span class="sxs-lookup"><span data-stu-id="c6648-391">dragSource</span></span>  

<!-- -->

<span data-ttu-id="c6648-392">dragMode</span><span class="sxs-lookup"><span data-stu-id="c6648-392">dragMode</span></span>  

<!-- -->

<span data-ttu-id="c6648-393">x</span><span class="sxs-lookup"><span data-stu-id="c6648-393">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-394">y</span><span class="sxs-lookup"><span data-stu-id="c6648-394">y</span></span>  

### <a name="return-value---dragover"></a><span data-ttu-id="c6648-395">戻り値 - dragOver</span><span class="sxs-lookup"><span data-stu-id="c6648-395">Return Value - dragOver</span></span>

## <a name="method-dragoverex"></a><span data-ttu-id="c6648-396">メソッド dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c6648-396">Method dragOverEx</span></span>

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a><span data-ttu-id="c6648-397">パラメーター - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c6648-397">Parameters - dragOverEx</span></span>

<span data-ttu-id="c6648-398">dragSource</span><span class="sxs-lookup"><span data-stu-id="c6648-398">dragSource</span></span>  

<!-- -->

<span data-ttu-id="c6648-399">dragMode</span><span class="sxs-lookup"><span data-stu-id="c6648-399">dragMode</span></span>  

<!-- -->

<span data-ttu-id="c6648-400">x</span><span class="sxs-lookup"><span data-stu-id="c6648-400">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-401">y</span><span class="sxs-lookup"><span data-stu-id="c6648-401">y</span></span>  

### <a name="return-value---dragoverex"></a><span data-ttu-id="c6648-402">戻り値 - dragOverEx</span><span class="sxs-lookup"><span data-stu-id="c6648-402">Return Value - dragOverEx</span></span>

## <a name="method-dragtext"></a><span data-ttu-id="c6648-403">メソッド dragText</span><span class="sxs-lookup"><span data-stu-id="c6648-403">Method dragText</span></span>

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a><span data-ttu-id="c6648-404">戻り値 - dragText</span><span class="sxs-lookup"><span data-stu-id="c6648-404">Return Value - dragText</span></span>

## <a name="method-enabled"></a><span data-ttu-id="c6648-405">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="c6648-405">Method enabled</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="c6648-406">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="c6648-406">Parameters - enabled</span></span>

<span data-ttu-id="c6648-407">値</span><span class="sxs-lookup"><span data-stu-id="c6648-407">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="c6648-408">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="c6648-408">Return Value - enabled</span></span>

## <a name="method-haschanged"></a><span data-ttu-id="c6648-409">メソッド hasChanged</span><span class="sxs-lookup"><span data-stu-id="c6648-409">Method hasChanged</span></span>

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a><span data-ttu-id="c6648-410">パラメーター - hasChanged</span><span class="sxs-lookup"><span data-stu-id="c6648-410">Parameters - hasChanged</span></span>

<span data-ttu-id="c6648-411">val</span><span class="sxs-lookup"><span data-stu-id="c6648-411">val</span></span>  

### <a name="return-value---haschanged"></a><span data-ttu-id="c6648-412">戻り値 - hasChanged</span><span class="sxs-lookup"><span data-stu-id="c6648-412">Return Value - hasChanged</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="c6648-413">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c6648-413">Method hasUserSetting</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="c6648-414">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="c6648-414">Return Value - hasUserSetting</span></span>

## <a name="method-height"></a><span data-ttu-id="c6648-415">メソッド height</span><span class="sxs-lookup"><span data-stu-id="c6648-415">Method height</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="c6648-416">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="c6648-416">Parameters - height</span></span>

<span data-ttu-id="c6648-417">値</span><span class="sxs-lookup"><span data-stu-id="c6648-417">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-418">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-418">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="c6648-419">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="c6648-419">Return Value - height</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="c6648-420">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="c6648-420">Method heightMode</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="c6648-421">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="c6648-421">Parameters - heightMode</span></span>

<span data-ttu-id="c6648-422">値</span><span class="sxs-lookup"><span data-stu-id="c6648-422">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="c6648-423">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="c6648-423">Return Value - heightMode</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="c6648-424">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="c6648-424">Method heightValue</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="c6648-425">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="c6648-425">Parameters - heightValue</span></span>

<span data-ttu-id="c6648-426">値</span><span class="sxs-lookup"><span data-stu-id="c6648-426">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="c6648-427">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="c6648-427">Return Value - heightValue</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="c6648-428">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="c6648-428">Method helpField</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="c6648-429">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="c6648-429">Return Value - helpField</span></span>

## <a name="method-helptext"></a><span data-ttu-id="c6648-430">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="c6648-430">Method helpText</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="c6648-431">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="c6648-431">Parameters - helpText</span></span>

<span data-ttu-id="c6648-432">値</span><span class="sxs-lookup"><span data-stu-id="c6648-432">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="c6648-433">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="c6648-433">Return Value - helpText</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="c6648-434">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="c6648-434">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="c6648-435">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="c6648-435">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="c6648-436">値</span><span class="sxs-lookup"><span data-stu-id="c6648-436">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="c6648-437">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="c6648-437">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="c6648-438">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c6648-438">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="c6648-439">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c6648-439">Parameters - hierarchyParent</span></span>

<span data-ttu-id="c6648-440">値</span><span class="sxs-lookup"><span data-stu-id="c6648-440">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="c6648-441">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="c6648-441">Return Value - hierarchyParent</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="c6648-442">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="c6648-442">Method hWnd</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="c6648-443">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="c6648-443">Return Value - hWnd</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="c6648-444">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="c6648-444">Method isContainer</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="c6648-445">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="c6648-445">Return Value - isContainer</span></span>

## <a name="method-isdisplayed"></a><span data-ttu-id="c6648-446">メソッド isDisplayed</span><span class="sxs-lookup"><span data-stu-id="c6648-446">Method isDisplayed</span></span>

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a><span data-ttu-id="c6648-447">戻り値 - isDisplayed</span><span class="sxs-lookup"><span data-stu-id="c6648-447">Return Value - isDisplayed</span></span>

## <a name="method-isrestricted"></a><span data-ttu-id="c6648-448">メソッド isRestricted</span><span class="sxs-lookup"><span data-stu-id="c6648-448">Method isRestricted</span></span>

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a><span data-ttu-id="c6648-449">戻り値 - isRestricted</span><span class="sxs-lookup"><span data-stu-id="c6648-449">Return Value - isRestricted</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="c6648-450">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c6648-450">Method isUserSetupEnabled</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="c6648-451">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c6648-451">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="c6648-452">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="c6648-452">neededSetupRights</span></span>  

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="c6648-453">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="c6648-453">Return Value - isUserSetupEnabled</span></span>

## <a name="method-isvisible"></a><span data-ttu-id="c6648-454">メソッド isVisible</span><span class="sxs-lookup"><span data-stu-id="c6648-454">Method isVisible</span></span>

```xpp
public boolean isVisible()
```

### <a name="return-value---isvisible"></a><span data-ttu-id="c6648-455">戻り値 - isVisible</span><span class="sxs-lookup"><span data-stu-id="c6648-455">Return Value - isVisible</span></span>

## <a name="method-isvisibleonclient"></a><span data-ttu-id="c6648-456">メソッド isVisibleOnClient</span><span class="sxs-lookup"><span data-stu-id="c6648-456">Method isVisibleOnClient</span></span>

```xpp
public boolean isVisibleOnClient()
```

### <a name="return-value---isvisibleonclient"></a><span data-ttu-id="c6648-457">戻り値 - isVisibleOnClient</span><span class="sxs-lookup"><span data-stu-id="c6648-457">Return Value - isVisibleOnClient</span></span>

## <a name="method-left"></a><span data-ttu-id="c6648-458">メソッド left</span><span class="sxs-lookup"><span data-stu-id="c6648-458">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="c6648-459">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="c6648-459">Parameters - left</span></span>

<span data-ttu-id="c6648-460">値</span><span class="sxs-lookup"><span data-stu-id="c6648-460">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-461">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-461">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="c6648-462">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="c6648-462">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="c6648-463">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-463">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="c6648-464">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-464">Parameters - leftMargin</span></span>

<span data-ttu-id="c6648-465">値</span><span class="sxs-lookup"><span data-stu-id="c6648-465">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-466">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-466">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="c6648-467">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-467">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="c6648-468">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-468">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="c6648-469">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-469">Parameters - leftMarginMode</span></span>

<span data-ttu-id="c6648-470">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-470">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="c6648-471">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-471">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="c6648-472">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-472">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="c6648-473">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-473">Parameters - leftMarginValue</span></span>

<span data-ttu-id="c6648-474">値</span><span class="sxs-lookup"><span data-stu-id="c6648-474">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="c6648-475">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-475">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="c6648-476">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="c6648-476">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="c6648-477">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="c6648-477">Parameters - leftMode</span></span>

<span data-ttu-id="c6648-478">値</span><span class="sxs-lookup"><span data-stu-id="c6648-478">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="c6648-479">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="c6648-479">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="c6648-480">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="c6648-480">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="c6648-481">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="c6648-481">Parameters - leftValue</span></span>

<span data-ttu-id="c6648-482">値</span><span class="sxs-lookup"><span data-stu-id="c6648-482">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="c6648-483">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="c6648-483">Return Value - leftValue</span></span>

## <a name="method-markasuseradd"></a><span data-ttu-id="c6648-484">メソッド markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c6648-484">Method markAsUserAdd</span></span>

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a><span data-ttu-id="c6648-485">パラメーター - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c6648-485">Parameters - markAsUserAdd</span></span>

<span data-ttu-id="c6648-486">値</span><span class="sxs-lookup"><span data-stu-id="c6648-486">value</span></span>  

### <a name="return-value---markasuseradd"></a><span data-ttu-id="c6648-487">戻り値 - markAsUserAdd</span><span class="sxs-lookup"><span data-stu-id="c6648-487">Return Value - markAsUserAdd</span></span>

## <a name="method-mousedblclick"></a><span data-ttu-id="c6648-488">メソッド mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c6648-488">Method mouseDblClick</span></span>

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a><span data-ttu-id="c6648-489">パラメーター - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c6648-489">Parameters - mouseDblClick</span></span>

<span data-ttu-id="c6648-490">x</span><span class="sxs-lookup"><span data-stu-id="c6648-490">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-491">y</span><span class="sxs-lookup"><span data-stu-id="c6648-491">y</span></span>  

<!-- -->

<span data-ttu-id="c6648-492">ボタン</span><span class="sxs-lookup"><span data-stu-id="c6648-492">button</span></span>  

<!-- -->

<span data-ttu-id="c6648-493">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c6648-493">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="c6648-494">Shift</span><span class="sxs-lookup"><span data-stu-id="c6648-494">Shift</span></span>  

### <a name="return-value---mousedblclick"></a><span data-ttu-id="c6648-495">戻り値 - mouseDblClick</span><span class="sxs-lookup"><span data-stu-id="c6648-495">Return Value - mouseDblClick</span></span>

## <a name="method-mousedown"></a><span data-ttu-id="c6648-496">メソッド mouseDown</span><span class="sxs-lookup"><span data-stu-id="c6648-496">Method mouseDown</span></span>

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a><span data-ttu-id="c6648-497">パラメーター - mouseDown</span><span class="sxs-lookup"><span data-stu-id="c6648-497">Parameters - mouseDown</span></span>

<span data-ttu-id="c6648-498">x</span><span class="sxs-lookup"><span data-stu-id="c6648-498">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-499">y</span><span class="sxs-lookup"><span data-stu-id="c6648-499">y</span></span>  

<!-- -->

<span data-ttu-id="c6648-500">ボタン</span><span class="sxs-lookup"><span data-stu-id="c6648-500">button</span></span>  

<!-- -->

<span data-ttu-id="c6648-501">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c6648-501">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="c6648-502">Shift</span><span class="sxs-lookup"><span data-stu-id="c6648-502">Shift</span></span>  

### <a name="return-value---mousedown"></a><span data-ttu-id="c6648-503">戻り値 - mouseDown</span><span class="sxs-lookup"><span data-stu-id="c6648-503">Return Value - mouseDown</span></span>

## <a name="method-mousemove"></a><span data-ttu-id="c6648-504">メソッド mouseMove</span><span class="sxs-lookup"><span data-stu-id="c6648-504">Method mouseMove</span></span>

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a><span data-ttu-id="c6648-505">パラメーター - mouseMove</span><span class="sxs-lookup"><span data-stu-id="c6648-505">Parameters - mouseMove</span></span>

<span data-ttu-id="c6648-506">x</span><span class="sxs-lookup"><span data-stu-id="c6648-506">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-507">y</span><span class="sxs-lookup"><span data-stu-id="c6648-507">y</span></span>  

<!-- -->

<span data-ttu-id="c6648-508">ボタン</span><span class="sxs-lookup"><span data-stu-id="c6648-508">button</span></span>  

<!-- -->

<span data-ttu-id="c6648-509">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c6648-509">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="c6648-510">Shift</span><span class="sxs-lookup"><span data-stu-id="c6648-510">Shift</span></span>  

### <a name="return-value---mousemove"></a><span data-ttu-id="c6648-511">戻り値 - mouseMove</span><span class="sxs-lookup"><span data-stu-id="c6648-511">Return Value - mouseMove</span></span>

## <a name="method-mouseup"></a><span data-ttu-id="c6648-512">メソッド mouseUp</span><span class="sxs-lookup"><span data-stu-id="c6648-512">Method mouseUp</span></span>

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a><span data-ttu-id="c6648-513">パラメーター - mouseUp</span><span class="sxs-lookup"><span data-stu-id="c6648-513">Parameters - mouseUp</span></span>

<span data-ttu-id="c6648-514">x</span><span class="sxs-lookup"><span data-stu-id="c6648-514">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-515">y</span><span class="sxs-lookup"><span data-stu-id="c6648-515">y</span></span>  

<!-- -->

<span data-ttu-id="c6648-516">ボタン</span><span class="sxs-lookup"><span data-stu-id="c6648-516">button</span></span>  

<!-- -->

<span data-ttu-id="c6648-517">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c6648-517">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="c6648-518">Shift</span><span class="sxs-lookup"><span data-stu-id="c6648-518">Shift</span></span>  

### <a name="return-value---mouseup"></a><span data-ttu-id="c6648-519">戻り値 - mouseUp</span><span class="sxs-lookup"><span data-stu-id="c6648-519">Return Value - mouseUp</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="c6648-520">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="c6648-520">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="c6648-521">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="c6648-521">Parameters - moveControl</span></span>

<span data-ttu-id="c6648-522">controlId</span><span class="sxs-lookup"><span data-stu-id="c6648-522">controlId</span></span>  

<!-- -->

<span data-ttu-id="c6648-523">insertAfterId</span><span class="sxs-lookup"><span data-stu-id="c6648-523">insertAfterId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="c6648-524">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="c6648-524">Return Value - moveControl</span></span>

## <a name="method-name"></a><span data-ttu-id="c6648-525">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c6648-525">Method name</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="c6648-526">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="c6648-526">Parameters - name</span></span>

<span data-ttu-id="c6648-527">値</span><span class="sxs-lookup"><span data-stu-id="c6648-527">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="c6648-528">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c6648-528">Return Value - name</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="c6648-529">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="c6648-529">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="c6648-530">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c6648-530">Parameters - neededPermission</span></span>

<span data-ttu-id="c6648-531">値</span><span class="sxs-lookup"><span data-stu-id="c6648-531">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="c6648-532">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="c6648-532">Return Value - neededPermission</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c6648-533">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c6648-533">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c6648-534">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c6648-534">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-parentcontrol"></a><span data-ttu-id="c6648-535">メソッド parentControl</span><span class="sxs-lookup"><span data-stu-id="c6648-535">Method parentControl</span></span>

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a><span data-ttu-id="c6648-536">戻り値 - parentControl</span><span class="sxs-lookup"><span data-stu-id="c6648-536">Return Value - parentControl</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="c6648-537">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-537">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="c6648-538">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-538">Parameters - rightMargin</span></span>

<span data-ttu-id="c6648-539">値</span><span class="sxs-lookup"><span data-stu-id="c6648-539">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-540">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-540">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="c6648-541">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-541">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="c6648-542">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-542">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="c6648-543">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-543">Parameters - rightMarginMode</span></span>

<span data-ttu-id="c6648-544">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-544">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="c6648-545">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-545">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="c6648-546">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-546">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="c6648-547">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-547">Parameters - rightMarginValue</span></span>

<span data-ttu-id="c6648-548">値</span><span class="sxs-lookup"><span data-stu-id="c6648-548">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="c6648-549">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-549">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="c6648-550">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="c6648-550">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="c6648-551">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="c6648-551">Parameters - securityKey</span></span>

<span data-ttu-id="c6648-552">値</span><span class="sxs-lookup"><span data-stu-id="c6648-552">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="c6648-553">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="c6648-553">Return Value - securityKey</span></span>

## <a name="method-showcontextmenu"></a><span data-ttu-id="c6648-554">メソッド showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c6648-554">Method showContextMenu</span></span>

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a><span data-ttu-id="c6648-555">パラメーター - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c6648-555">Parameters - showContextMenu</span></span>

<span data-ttu-id="c6648-556">menuHandle</span><span class="sxs-lookup"><span data-stu-id="c6648-556">menuHandle</span></span>  

### <a name="return-value---showcontextmenu"></a><span data-ttu-id="c6648-557">戻り値 - showContextMenu</span><span class="sxs-lookup"><span data-stu-id="c6648-557">Return Value - showContextMenu</span></span>

## <a name="method-skip"></a><span data-ttu-id="c6648-558">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="c6648-558">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="c6648-559">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="c6648-559">Parameters - skip</span></span>

<span data-ttu-id="c6648-560">値</span><span class="sxs-lookup"><span data-stu-id="c6648-560">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="c6648-561">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="c6648-561">Return Value - skip</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="c6648-562">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="c6648-562">Method toolTip</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="c6648-563">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="c6648-563">Return Value - toolTip</span></span>

## <a name="method-top"></a><span data-ttu-id="c6648-564">メソッド top</span><span class="sxs-lookup"><span data-stu-id="c6648-564">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="c6648-565">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="c6648-565">Parameters - top</span></span>

<span data-ttu-id="c6648-566">値</span><span class="sxs-lookup"><span data-stu-id="c6648-566">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-567">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-567">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="c6648-568">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="c6648-568">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="c6648-569">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-569">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="c6648-570">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-570">Parameters - topMargin</span></span>

<span data-ttu-id="c6648-571">値</span><span class="sxs-lookup"><span data-stu-id="c6648-571">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-572">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-572">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="c6648-573">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="c6648-573">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="c6648-574">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-574">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="c6648-575">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-575">Parameters - topMarginMode</span></span>

<span data-ttu-id="c6648-576">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-576">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="c6648-577">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="c6648-577">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="c6648-578">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-578">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="c6648-579">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-579">Parameters - topMarginValue</span></span>

<span data-ttu-id="c6648-580">値</span><span class="sxs-lookup"><span data-stu-id="c6648-580">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="c6648-581">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="c6648-581">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="c6648-582">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="c6648-582">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="c6648-583">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="c6648-583">Parameters - topMode</span></span>

<span data-ttu-id="c6648-584">値</span><span class="sxs-lookup"><span data-stu-id="c6648-584">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="c6648-585">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="c6648-585">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="c6648-586">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="c6648-586">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="c6648-587">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="c6648-587">Parameters - topValue</span></span>

<span data-ttu-id="c6648-588">値</span><span class="sxs-lookup"><span data-stu-id="c6648-588">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="c6648-589">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="c6648-589">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="c6648-590">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="c6648-590">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="c6648-591">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="c6648-591">Parameters - type</span></span>

<span data-ttu-id="c6648-592">値</span><span class="sxs-lookup"><span data-stu-id="c6648-592">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="c6648-593">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="c6648-593">Return Value - type</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="c6648-594">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c6648-594">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="c6648-595">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c6648-595">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="c6648-596">データ</span><span class="sxs-lookup"><span data-stu-id="c6648-596">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="c6648-597">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="c6648-597">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-userdata"></a><span data-ttu-id="c6648-598">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="c6648-598">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="c6648-599">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="c6648-599">Parameters - userData</span></span>

<span data-ttu-id="c6648-600">値</span><span class="sxs-lookup"><span data-stu-id="c6648-600">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="c6648-601">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="c6648-601">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="c6648-602">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="c6648-602">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="c6648-603">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="c6648-603">Parameters - userDataItem</span></span>

<span data-ttu-id="c6648-604">値</span><span class="sxs-lookup"><span data-stu-id="c6648-604">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="c6648-605">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="c6648-605">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="c6648-606">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="c6648-606">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="c6648-607">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="c6648-607">Parameters - userDataItems</span></span>

<span data-ttu-id="c6648-608">値</span><span class="sxs-lookup"><span data-stu-id="c6648-608">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="c6648-609">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="c6648-609">Return Value - userDataItems</span></span>

## <a name="method-userdisable"></a><span data-ttu-id="c6648-610">メソッド userDisable</span><span class="sxs-lookup"><span data-stu-id="c6648-610">Method userDisable</span></span>

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a><span data-ttu-id="c6648-611">パラメーター - userDisable</span><span class="sxs-lookup"><span data-stu-id="c6648-611">Parameters - userDisable</span></span>

<span data-ttu-id="c6648-612">値</span><span class="sxs-lookup"><span data-stu-id="c6648-612">value</span></span>  

### <a name="return-value---userdisable"></a><span data-ttu-id="c6648-613">戻り値 - userDisable</span><span class="sxs-lookup"><span data-stu-id="c6648-613">Return Value - userDisable</span></span>

## <a name="method-userheight"></a><span data-ttu-id="c6648-614">メソッド userHeight</span><span class="sxs-lookup"><span data-stu-id="c6648-614">Method userHeight</span></span>

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a><span data-ttu-id="c6648-615">パラメーター - userHeight</span><span class="sxs-lookup"><span data-stu-id="c6648-615">Parameters - userHeight</span></span>

<span data-ttu-id="c6648-616">値</span><span class="sxs-lookup"><span data-stu-id="c6648-616">value</span></span>  

### <a name="return-value---userheight"></a><span data-ttu-id="c6648-617">戻り値 - userHeight</span><span class="sxs-lookup"><span data-stu-id="c6648-617">Return Value - userHeight</span></span>

## <a name="method-userhide"></a><span data-ttu-id="c6648-618">メソッド userHide</span><span class="sxs-lookup"><span data-stu-id="c6648-618">Method userHide</span></span>

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a><span data-ttu-id="c6648-619">パラメーター - userHide</span><span class="sxs-lookup"><span data-stu-id="c6648-619">Parameters - userHide</span></span>

<span data-ttu-id="c6648-620">値</span><span class="sxs-lookup"><span data-stu-id="c6648-620">value</span></span>  

### <a name="return-value---userhide"></a><span data-ttu-id="c6648-621">戻り値 - userHide</span><span class="sxs-lookup"><span data-stu-id="c6648-621">Return Value - userHide</span></span>

## <a name="method-userorgcontainer"></a><span data-ttu-id="c6648-622">メソッド userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c6648-622">Method userOrgContainer</span></span>

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a><span data-ttu-id="c6648-623">パラメーター - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c6648-623">Parameters - userOrgContainer</span></span>

<span data-ttu-id="c6648-624">値</span><span class="sxs-lookup"><span data-stu-id="c6648-624">value</span></span>  

### <a name="return-value---userorgcontainer"></a><span data-ttu-id="c6648-625">戻り値 - userOrgContainer</span><span class="sxs-lookup"><span data-stu-id="c6648-625">Return Value - userOrgContainer</span></span>

## <a name="method-userorgsibling"></a><span data-ttu-id="c6648-626">メソッド userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c6648-626">Method userOrgSibling</span></span>

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a><span data-ttu-id="c6648-627">パラメーター - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c6648-627">Parameters - userOrgSibling</span></span>

<span data-ttu-id="c6648-628">値</span><span class="sxs-lookup"><span data-stu-id="c6648-628">value</span></span>  

### <a name="return-value---userorgsibling"></a><span data-ttu-id="c6648-629">戻り値 - userOrgSibling</span><span class="sxs-lookup"><span data-stu-id="c6648-629">Return Value - userOrgSibling</span></span>

## <a name="method-userprompttext"></a><span data-ttu-id="c6648-630">メソッド userPromptText</span><span class="sxs-lookup"><span data-stu-id="c6648-630">Method userPromptText</span></span>

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a><span data-ttu-id="c6648-631">パラメーター - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c6648-631">Parameters - userPromptText</span></span>

<span data-ttu-id="c6648-632">値</span><span class="sxs-lookup"><span data-stu-id="c6648-632">value</span></span>  

### <a name="return-value---userprompttext"></a><span data-ttu-id="c6648-633">戻り値 - userPromptText</span><span class="sxs-lookup"><span data-stu-id="c6648-633">Return Value - userPromptText</span></span>

## <a name="method-usersecuritylevel"></a><span data-ttu-id="c6648-634">メソッド userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c6648-634">Method userSecurityLevel</span></span>

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a><span data-ttu-id="c6648-635">パラメーター - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c6648-635">Parameters - userSecurityLevel</span></span>

<span data-ttu-id="c6648-636">値</span><span class="sxs-lookup"><span data-stu-id="c6648-636">value</span></span>  

### <a name="return-value---usersecuritylevel"></a><span data-ttu-id="c6648-637">戻り値 - userSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c6648-637">Return Value - userSecurityLevel</span></span>

## <a name="method-userskip"></a><span data-ttu-id="c6648-638">メソッド userSkip</span><span class="sxs-lookup"><span data-stu-id="c6648-638">Method userSkip</span></span>

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a><span data-ttu-id="c6648-639">パラメーター - userSkip</span><span class="sxs-lookup"><span data-stu-id="c6648-639">Parameters - userSkip</span></span>

<span data-ttu-id="c6648-640">値</span><span class="sxs-lookup"><span data-stu-id="c6648-640">value</span></span>  

### <a name="return-value---userskip"></a><span data-ttu-id="c6648-641">戻り値 - userSkip</span><span class="sxs-lookup"><span data-stu-id="c6648-641">Return Value - userSkip</span></span>

## <a name="method-userwidth"></a><span data-ttu-id="c6648-642">メソッド userWidth</span><span class="sxs-lookup"><span data-stu-id="c6648-642">Method userWidth</span></span>

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a><span data-ttu-id="c6648-643">パラメーター - userWidth</span><span class="sxs-lookup"><span data-stu-id="c6648-643">Parameters - userWidth</span></span>

<span data-ttu-id="c6648-644">値</span><span class="sxs-lookup"><span data-stu-id="c6648-644">value</span></span>  

### <a name="return-value---userwidth"></a><span data-ttu-id="c6648-645">戻り値 - userWidth</span><span class="sxs-lookup"><span data-stu-id="c6648-645">Return Value - userWidth</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="c6648-646">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="c6648-646">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="c6648-647">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="c6648-647">Parameters - useUserLayout</span></span>

<span data-ttu-id="c6648-648">値</span><span class="sxs-lookup"><span data-stu-id="c6648-648">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="c6648-649">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="c6648-649">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="c6648-650">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c6648-650">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="c6648-651">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c6648-651">Parameters - verticalSpacing</span></span>

<span data-ttu-id="c6648-652">値</span><span class="sxs-lookup"><span data-stu-id="c6648-652">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-653">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-653">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="c6648-654">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="c6648-654">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="c6648-655">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c6648-655">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="c6648-656">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c6648-656">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="c6648-657">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-657">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="c6648-658">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="c6648-658">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="c6648-659">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c6648-659">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="c6648-660">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c6648-660">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="c6648-661">値</span><span class="sxs-lookup"><span data-stu-id="c6648-661">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="c6648-662">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="c6648-662">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="c6648-663">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="c6648-663">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="c6648-664">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="c6648-664">Parameters - visible</span></span>

<span data-ttu-id="c6648-665">値</span><span class="sxs-lookup"><span data-stu-id="c6648-665">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="c6648-666">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="c6648-666">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="c6648-667">メソッド width</span><span class="sxs-lookup"><span data-stu-id="c6648-667">Method width</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="c6648-668">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="c6648-668">Parameters - width</span></span>

<span data-ttu-id="c6648-669">値</span><span class="sxs-lookup"><span data-stu-id="c6648-669">value</span></span>  

<!-- -->

<span data-ttu-id="c6648-670">モード</span><span class="sxs-lookup"><span data-stu-id="c6648-670">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="c6648-671">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="c6648-671">Return Value - width</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="c6648-672">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="c6648-672">Method widthMode</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="c6648-673">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="c6648-673">Parameters - widthMode</span></span>

<span data-ttu-id="c6648-674">値</span><span class="sxs-lookup"><span data-stu-id="c6648-674">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="c6648-675">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="c6648-675">Return Value - widthMode</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="c6648-676">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="c6648-676">Method widthValue</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="c6648-677">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="c6648-677">Parameters - widthValue</span></span>

<span data-ttu-id="c6648-678">値</span><span class="sxs-lookup"><span data-stu-id="c6648-678">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="c6648-679">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="c6648-679">Return Value - widthValue</span></span>

## <a name="method-dropex"></a><span data-ttu-id="c6648-680">メソッド dropEx</span><span class="sxs-lookup"><span data-stu-id="c6648-680">Method dropEx</span></span>

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a><span data-ttu-id="c6648-681">パラメーター - dropEx</span><span class="sxs-lookup"><span data-stu-id="c6648-681">Parameters - dropEx</span></span>

<span data-ttu-id="c6648-682">dragSource</span><span class="sxs-lookup"><span data-stu-id="c6648-682">dragSource</span></span>  

<!-- -->

<span data-ttu-id="c6648-683">dragMode</span><span class="sxs-lookup"><span data-stu-id="c6648-683">dragMode</span></span>  

<!-- -->

<span data-ttu-id="c6648-684">x</span><span class="sxs-lookup"><span data-stu-id="c6648-684">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-685">y</span><span class="sxs-lookup"><span data-stu-id="c6648-685">y</span></span>  

## <a name="method-inputsearch"></a><span data-ttu-id="c6648-686">メソッド inputSearch</span><span class="sxs-lookup"><span data-stu-id="c6648-686">Method inputSearch</span></span>

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a><span data-ttu-id="c6648-687">パラメーター - inputSearch</span><span class="sxs-lookup"><span data-stu-id="c6648-687">Parameters - inputSearch</span></span>

<span data-ttu-id="c6648-688">searchStr</span><span class="sxs-lookup"><span data-stu-id="c6648-688">searchStr</span></span>  

## <a name="method-prefcolumnsize"></a><span data-ttu-id="c6648-689">メソッド prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="c6648-689">Method prefColumnSize</span></span>

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a><span data-ttu-id="c6648-690">パラメーター - prefColumnSize</span><span class="sxs-lookup"><span data-stu-id="c6648-690">Parameters - prefColumnSize</span></span>

<span data-ttu-id="c6648-691">width</span><span class="sxs-lookup"><span data-stu-id="c6648-691">width</span></span>  

<!-- -->

<span data-ttu-id="c6648-692">height</span><span class="sxs-lookup"><span data-stu-id="c6648-692">height</span></span>  

## <a name="method-gotfocus"></a><span data-ttu-id="c6648-693">メソッド gotFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-693">Method gotFocus</span></span>

```xpp
public void gotFocus()
```

## <a name="method-lostfocus"></a><span data-ttu-id="c6648-694">メソッド lostFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-694">Method lostFocus</span></span>

```xpp
public void lostFocus()
```

## <a name="method-mouseleave"></a><span data-ttu-id="c6648-695">メソッド mouseLeave</span><span class="sxs-lookup"><span data-stu-id="c6648-695">Method mouseLeave</span></span>

```xpp
public void mouseLeave()
```

## <a name="method-setfocus"></a><span data-ttu-id="c6648-696">メソッド setFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-696">Method setFocus</span></span>

```xpp
public void setFocus()
```

## <a name="method-copy"></a><span data-ttu-id="c6648-697">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="c6648-697">Method copy</span></span>

```xpp
public void copy()
```

## <a name="method-ongotfocus"></a><span data-ttu-id="c6648-698">メソッド OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-698">Method OnGotFocus</span></span>

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a><span data-ttu-id="c6648-699">パラメーター - OnGotFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-699">Parameters - OnGotFocus</span></span>

<span data-ttu-id="c6648-700">sender</span><span class="sxs-lookup"><span data-stu-id="c6648-700">sender</span></span>  

<!-- -->

<span data-ttu-id="c6648-701">e</span><span class="sxs-lookup"><span data-stu-id="c6648-701">e</span></span>  

## <a name="method-displaycontrol"></a><span data-ttu-id="c6648-702">メソッド displayControl</span><span class="sxs-lookup"><span data-stu-id="c6648-702">Method displayControl</span></span>

```xpp
public void displayControl()
```

## <a name="method-paste"></a><span data-ttu-id="c6648-703">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="c6648-703">Method paste</span></span>

```xpp
public void paste()
```

## <a name="method-drop"></a><span data-ttu-id="c6648-704">メソッド drop</span><span class="sxs-lookup"><span data-stu-id="c6648-704">Method drop</span></span>

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a><span data-ttu-id="c6648-705">パラメーター - drop</span><span class="sxs-lookup"><span data-stu-id="c6648-705">Parameters - drop</span></span>

<span data-ttu-id="c6648-706">dragSource</span><span class="sxs-lookup"><span data-stu-id="c6648-706">dragSource</span></span>  

<!-- -->

<span data-ttu-id="c6648-707">dragMode</span><span class="sxs-lookup"><span data-stu-id="c6648-707">dragMode</span></span>  

<!-- -->

<span data-ttu-id="c6648-708">x</span><span class="sxs-lookup"><span data-stu-id="c6648-708">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-709">y</span><span class="sxs-lookup"><span data-stu-id="c6648-709">y</span></span>  

## <a name="method-onlostfocus"></a><span data-ttu-id="c6648-710">メソッド OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-710">Method OnLostFocus</span></span>

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a><span data-ttu-id="c6648-711">パラメーター - OnLostFocus</span><span class="sxs-lookup"><span data-stu-id="c6648-711">Parameters - OnLostFocus</span></span>

<span data-ttu-id="c6648-712">sender</span><span class="sxs-lookup"><span data-stu-id="c6648-712">sender</span></span>  

<!-- -->

<span data-ttu-id="c6648-713">e</span><span class="sxs-lookup"><span data-stu-id="c6648-713">e</span></span>  

## <a name="method-mouseenter"></a><span data-ttu-id="c6648-714">メソッド mouseEnter</span><span class="sxs-lookup"><span data-stu-id="c6648-714">Method mouseEnter</span></span>

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a><span data-ttu-id="c6648-715">パラメーター - mouseEnter</span><span class="sxs-lookup"><span data-stu-id="c6648-715">Parameters - mouseEnter</span></span>

<span data-ttu-id="c6648-716">x</span><span class="sxs-lookup"><span data-stu-id="c6648-716">x</span></span>  

<!-- -->

<span data-ttu-id="c6648-717">y</span><span class="sxs-lookup"><span data-stu-id="c6648-717">y</span></span>  

<!-- -->

<span data-ttu-id="c6648-718">ボタン</span><span class="sxs-lookup"><span data-stu-id="c6648-718">button</span></span>  

<!-- -->

<span data-ttu-id="c6648-719">Ctrl</span><span class="sxs-lookup"><span data-stu-id="c6648-719">Ctrl</span></span>  

<!-- -->

<span data-ttu-id="c6648-720">Shift</span><span class="sxs-lookup"><span data-stu-id="c6648-720">Shift</span></span>  

## <a name="method-resetusersetting"></a><span data-ttu-id="c6648-721">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="c6648-721">Method resetUserSetting</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-enddrag"></a><span data-ttu-id="c6648-722">メソッド endDrag</span><span class="sxs-lookup"><span data-stu-id="c6648-722">Method endDrag</span></span>

```xpp
public void endDrag()
```

## <a name="method-arrange"></a><span data-ttu-id="c6648-723">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="c6648-723">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-dragleave"></a><span data-ttu-id="c6648-724">メソッド dragLeave</span><span class="sxs-lookup"><span data-stu-id="c6648-724">Method dragLeave</span></span>

```xpp
public void dragLeave()
```

## <a name="method-cut"></a><span data-ttu-id="c6648-725">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="c6648-725">Method cut</span></span>

```xpp
public void cut()
```

## <a name="method-registeroverridemethod"></a><span data-ttu-id="c6648-726">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="c6648-726">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="c6648-727">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="c6648-727">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="c6648-728">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="c6648-728">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="c6648-729">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="c6648-729">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="c6648-730">overrideObject</span><span class="sxs-lookup"><span data-stu-id="c6648-730">overrideObject</span></span>  

## <a name="method-context"></a><span data-ttu-id="c6648-731">メソッド context</span><span class="sxs-lookup"><span data-stu-id="c6648-731">Method context</span></span>

```xpp
public void context()
```

