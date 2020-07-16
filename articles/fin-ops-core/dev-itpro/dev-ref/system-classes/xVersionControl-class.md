---
title: xVersionControl クラス
description: このトピックでは、xVersionControl クラスについて説明します。
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
ms.openlocfilehash: f9ea8c0a2e9c1343bbdc32d074319ba694948457
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502757"
---
# <a name="class-xversioncontrol"></a><span data-ttu-id="a6996-103">クラス xVersionControl</span><span class="sxs-lookup"><span data-stu-id="a6996-103">Class xVersionControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xVersionControl extends Object
```

## <a name="remarks"></a><span data-ttu-id="a6996-104">備考</span><span class="sxs-lookup"><span data-stu-id="a6996-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a6996-105">例</span><span class="sxs-lookup"><span data-stu-id="a6996-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a6996-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a6996-106">Methods</span></span>

| <span data-ttu-id="a6996-107">方法</span><span class="sxs-lookup"><span data-stu-id="a6996-107">Method</span></span>                                                                                                                                                            | <span data-ttu-id="a6996-108">説明</span><span class="sxs-lookup"><span data-stu-id="a6996-108">Description</span></span>                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a6996-109">public boolean allowCreate(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-109">public boolean allowCreate(TreeNode node)</span></span>                                                                                                                         |                                                          |
| <span data-ttu-id="a6996-110">public boolean allowDelete(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-110">public boolean allowDelete(TreeNode node)</span></span>                                                                                                                         |                                                          |
| <span data-ttu-id="a6996-111">public boolean allowEdit(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-111">public boolean allowEdit(TreeNode node)</span></span>                                                                                                                           |                                                          |
| <span data-ttu-id="a6996-112">public boolean allowRename(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-112">public boolean allowRename(TreeNode node)</span></span>                                                                                                                         |                                                          |
| <span data-ttu-id="a6996-113">public boolean checkOut(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-113">public boolean checkOut(TreeNode node)</span></span>                                                                                                                            |                                                          |
| <span data-ttu-id="a6996-114">public boolean create(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-114">public boolean create(TreeNode node)</span></span>                                                                                                                              |                                                          |
| <span data-ttu-id="a6996-115">public boolean delete(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-115">public boolean delete(TreeNode node)</span></span>                                                                                                                              |                                                          |
| <span data-ttu-id="a6996-116">public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, \[int parentId\], \[IdAllocationSchema idAllocationSchema\], \[boolean inheritance\])</span><span class="sxs-lookup"><span data-stu-id="a6996-116">public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, \[int parentId\], \[IdAllocationSchema idAllocationSchema\], \[boolean inheritance\])</span></span> |                                                          |
| <span data-ttu-id="a6996-117">public int getAvailableLabelId(str labelFile, str language, \[IdAllocationSchema idAllocationSchema\])</span><span class="sxs-lookup"><span data-stu-id="a6996-117">public int getAvailableLabelId(str labelFile, str language, \[IdAllocationSchema idAllocationSchema\])</span></span>                                                            |                                                          |
| <span data-ttu-id="a6996-118">public boolean ideIntegration()</span><span class="sxs-lookup"><span data-stu-id="a6996-118">public boolean ideIntegration()</span></span>                                                                                                                                   |                                                          |
| <span data-ttu-id="a6996-119">public boolean moveToModel(TreeNode node, int modelId)</span><span class="sxs-lookup"><span data-stu-id="a6996-119">public boolean moveToModel(TreeNode node, int modelId)</span></span>                                                                                                            |                                                          |
| <span data-ttu-id="a6996-120">public boolean rename(TreeNode node, str newname)</span><span class="sxs-lookup"><span data-stu-id="a6996-120">public boolean rename(TreeNode node, str newname)</span></span>                                                                                                                 |                                                          |
| <span data-ttu-id="a6996-121">public boolean undoCheckOut(TreeNode node, \[boolean showDialog\])</span><span class="sxs-lookup"><span data-stu-id="a6996-121">public boolean undoCheckOut(TreeNode node, \[boolean showDialog\])</span></span>                                                                                                |                                                          |
| <span data-ttu-id="a6996-122">public Set unwantedObjectTypes()</span><span class="sxs-lookup"><span data-stu-id="a6996-122">public Set unwantedObjectTypes()</span></span>                                                                                                                                  |                                                          |
| <span data-ttu-id="a6996-123">public void colorAOT()</span><span class="sxs-lookup"><span data-stu-id="a6996-123">public void colorAOT()</span></span>                                                                                                                                            |                                                          |
| <span data-ttu-id="a6996-124">public void save(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-124">public void save(TreeNode node)</span></span>                                                                                                                                   |                                                          |
| <span data-ttu-id="a6996-125">public void showHistory(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-125">public void showHistory(TreeNode node)</span></span>                                                                                                                            |                                                          |
| <span data-ttu-id="a6996-126">public void updateCheckedOutList(Set checkedOutObjects)</span><span class="sxs-lookup"><span data-stu-id="a6996-126">public void updateCheckedOutList(Set checkedOutObjects)</span></span>                                                                                                           |                                                          |
| <span data-ttu-id="a6996-127">public void getLatestVersion(\[TreeNode node\], \[boolean delLocalFiles\])</span><span class="sxs-lookup"><span data-stu-id="a6996-127">public void getLatestVersion(\[TreeNode node\], \[boolean delLocalFiles\])</span></span>                                                                                        |                                                          |
| <span data-ttu-id="a6996-128">public void checkIn(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="a6996-128">public void checkIn(TreeNode node)</span></span>                                                                                                                                |                                                          |
| <span data-ttu-id="a6996-129">public void new()</span><span class="sxs-lookup"><span data-stu-id="a6996-129">public void new()</span></span>                                                                                                                                                 | <span data-ttu-id="a6996-130">xVersionControl クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6996-130">Initializes a new instance of the xVersionControl class.</span></span> |
| <span data-ttu-id="a6996-131">public void reload()</span><span class="sxs-lookup"><span data-stu-id="a6996-131">public void reload()</span></span>                                                                                                                                              |                                                          |
| <span data-ttu-id="a6996-132">public void getLabelVersion(\[TreeNode node\], \[str label\])</span><span class="sxs-lookup"><span data-stu-id="a6996-132">public void getLabelVersion(\[TreeNode node\], \[str label\])</span></span>                                                                                                     |                                                          |

## <a name="method-allowcreate"></a><span data-ttu-id="a6996-133">メソッド allowCreate</span><span class="sxs-lookup"><span data-stu-id="a6996-133">Method allowCreate</span></span>

```xpp
public boolean allowCreate(TreeNode node)
```

### <a name="parameters---allowcreate"></a><span data-ttu-id="a6996-134">パラメーター - allowCreate</span><span class="sxs-lookup"><span data-stu-id="a6996-134">Parameters - allowCreate</span></span>

<span data-ttu-id="a6996-135">node</span><span class="sxs-lookup"><span data-stu-id="a6996-135">node</span></span>  

### <a name="return-value---allowcreate"></a><span data-ttu-id="a6996-136">戻り値 - allowCreate</span><span class="sxs-lookup"><span data-stu-id="a6996-136">Return Value - allowCreate</span></span>

## <a name="method-allowdelete"></a><span data-ttu-id="a6996-137">メソッド allowDelete</span><span class="sxs-lookup"><span data-stu-id="a6996-137">Method allowDelete</span></span>

```xpp
public boolean allowDelete(TreeNode node)
```

### <a name="parameters---allowdelete"></a><span data-ttu-id="a6996-138">パラメーター - allowDelete</span><span class="sxs-lookup"><span data-stu-id="a6996-138">Parameters - allowDelete</span></span>

<span data-ttu-id="a6996-139">node</span><span class="sxs-lookup"><span data-stu-id="a6996-139">node</span></span>  

### <a name="return-value---allowdelete"></a><span data-ttu-id="a6996-140">戻り値 - allowDelete</span><span class="sxs-lookup"><span data-stu-id="a6996-140">Return Value - allowDelete</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="a6996-141">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="a6996-141">Method allowEdit</span></span>

```xpp
public boolean allowEdit(TreeNode node)
```

### <a name="parameters---allowedit"></a><span data-ttu-id="a6996-142">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a6996-142">Parameters - allowEdit</span></span>

<span data-ttu-id="a6996-143">node</span><span class="sxs-lookup"><span data-stu-id="a6996-143">node</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="a6996-144">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a6996-144">Return Value - allowEdit</span></span>

## <a name="method-allowrename"></a><span data-ttu-id="a6996-145">メソッド allowRename</span><span class="sxs-lookup"><span data-stu-id="a6996-145">Method allowRename</span></span>

```xpp
public boolean allowRename(TreeNode node)
```

### <a name="parameters---allowrename"></a><span data-ttu-id="a6996-146">パラメーター - allowRename</span><span class="sxs-lookup"><span data-stu-id="a6996-146">Parameters - allowRename</span></span>

<span data-ttu-id="a6996-147">node</span><span class="sxs-lookup"><span data-stu-id="a6996-147">node</span></span>  

### <a name="return-value---allowrename"></a><span data-ttu-id="a6996-148">戻り値 - allowRename</span><span class="sxs-lookup"><span data-stu-id="a6996-148">Return Value - allowRename</span></span>

## <a name="method-checkout"></a><span data-ttu-id="a6996-149">メソッド checkOut</span><span class="sxs-lookup"><span data-stu-id="a6996-149">Method checkOut</span></span>

```xpp
public boolean checkOut(TreeNode node)
```

### <a name="parameters---checkout"></a><span data-ttu-id="a6996-150">パラメーター - checkOut</span><span class="sxs-lookup"><span data-stu-id="a6996-150">Parameters - checkOut</span></span>

<span data-ttu-id="a6996-151">node</span><span class="sxs-lookup"><span data-stu-id="a6996-151">node</span></span>  

### <a name="return-value---checkout"></a><span data-ttu-id="a6996-152">戻り値 - checkOut</span><span class="sxs-lookup"><span data-stu-id="a6996-152">Return Value - checkOut</span></span>

## <a name="method-create"></a><span data-ttu-id="a6996-153">メソッド create</span><span class="sxs-lookup"><span data-stu-id="a6996-153">Method create</span></span>

```xpp
public boolean create(TreeNode node)
```

### <a name="parameters---create"></a><span data-ttu-id="a6996-154">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="a6996-154">Parameters - create</span></span>

<span data-ttu-id="a6996-155">node</span><span class="sxs-lookup"><span data-stu-id="a6996-155">node</span></span>  

### <a name="return-value---create"></a><span data-ttu-id="a6996-156">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="a6996-156">Return Value - create</span></span>

## <a name="method-delete"></a><span data-ttu-id="a6996-157">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="a6996-157">Method delete</span></span>

```xpp
public boolean delete(TreeNode node)
```

### <a name="parameters---delete"></a><span data-ttu-id="a6996-158">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="a6996-158">Parameters - delete</span></span>

<span data-ttu-id="a6996-159">node</span><span class="sxs-lookup"><span data-stu-id="a6996-159">node</span></span>  

### <a name="return-value---delete"></a><span data-ttu-id="a6996-160">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="a6996-160">Return Value - delete</span></span>

## <a name="method-getavailableid"></a><span data-ttu-id="a6996-161">メソッド getAvailableId</span><span class="sxs-lookup"><span data-stu-id="a6996-161">Method getAvailableId</span></span>

```xpp
public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, [int parentId], [IdAllocationSchema idAllocationSchema], [boolean inheritance])
```

### <a name="parameters---getavailableid"></a><span data-ttu-id="a6996-162">パラメーター - getAvailableId</span><span class="sxs-lookup"><span data-stu-id="a6996-162">Parameters - getAvailableId</span></span>

<span data-ttu-id="a6996-163">objectType</span><span class="sxs-lookup"><span data-stu-id="a6996-163">objectType</span></span>  

<!-- -->

<span data-ttu-id="a6996-164"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="a6996-164">layer</span></span>  

<!-- -->

<span data-ttu-id="a6996-165">parentId</span><span class="sxs-lookup"><span data-stu-id="a6996-165">parentId</span></span>  

<!-- -->

<span data-ttu-id="a6996-166">idAllocationSchema</span><span class="sxs-lookup"><span data-stu-id="a6996-166">idAllocationSchema</span></span>  

<!-- -->

<span data-ttu-id="a6996-167">inheritance</span><span class="sxs-lookup"><span data-stu-id="a6996-167">inheritance</span></span>  

### <a name="return-value---getavailableid"></a><span data-ttu-id="a6996-168">戻り値 - getAvailableId</span><span class="sxs-lookup"><span data-stu-id="a6996-168">Return Value - getAvailableId</span></span>

## <a name="method-getavailablelabelid"></a><span data-ttu-id="a6996-169">メソッド getAvailableLabelId</span><span class="sxs-lookup"><span data-stu-id="a6996-169">Method getAvailableLabelId</span></span>

```xpp
public int getAvailableLabelId(str labelFile, str language, [IdAllocationSchema idAllocationSchema])
```

### <a name="parameters---getavailablelabelid"></a><span data-ttu-id="a6996-170">パラメーター - getAvailableLabelId</span><span class="sxs-lookup"><span data-stu-id="a6996-170">Parameters - getAvailableLabelId</span></span>

<span data-ttu-id="a6996-171">labelFile</span><span class="sxs-lookup"><span data-stu-id="a6996-171">labelFile</span></span>  

<!-- -->

<span data-ttu-id="a6996-172">言語</span><span class="sxs-lookup"><span data-stu-id="a6996-172">language</span></span>  

<!-- -->

<span data-ttu-id="a6996-173">idAllocationSchema</span><span class="sxs-lookup"><span data-stu-id="a6996-173">idAllocationSchema</span></span>  

### <a name="return-value---getavailablelabelid"></a><span data-ttu-id="a6996-174">戻り値 - getAvailableLabelId</span><span class="sxs-lookup"><span data-stu-id="a6996-174">Return Value - getAvailableLabelId</span></span>

## <a name="method-ideintegration"></a><span data-ttu-id="a6996-175">メソッド ideIntegration</span><span class="sxs-lookup"><span data-stu-id="a6996-175">Method ideIntegration</span></span>

```xpp
public boolean ideIntegration()
```

### <a name="return-value---ideintegration"></a><span data-ttu-id="a6996-176">戻り値 - ideIntegration</span><span class="sxs-lookup"><span data-stu-id="a6996-176">Return Value - ideIntegration</span></span>

## <a name="method-movetomodel"></a><span data-ttu-id="a6996-177">メソッド moveToModel</span><span class="sxs-lookup"><span data-stu-id="a6996-177">Method moveToModel</span></span>

```xpp
public boolean moveToModel(TreeNode node, int modelId)
```

### <a name="parameters---movetomodel"></a><span data-ttu-id="a6996-178">パラメーター - moveToModel</span><span class="sxs-lookup"><span data-stu-id="a6996-178">Parameters - moveToModel</span></span>

<span data-ttu-id="a6996-179">node</span><span class="sxs-lookup"><span data-stu-id="a6996-179">node</span></span>  

<!-- -->

<span data-ttu-id="a6996-180">modelId</span><span class="sxs-lookup"><span data-stu-id="a6996-180">modelId</span></span>  

### <a name="return-value---movetomodel"></a><span data-ttu-id="a6996-181">戻り値 - moveToModel</span><span class="sxs-lookup"><span data-stu-id="a6996-181">Return Value - moveToModel</span></span>

## <a name="method-rename"></a><span data-ttu-id="a6996-182">メソッド rename</span><span class="sxs-lookup"><span data-stu-id="a6996-182">Method rename</span></span>

```xpp
public boolean rename(TreeNode node, str newname)
```

### <a name="parameters---rename"></a><span data-ttu-id="a6996-183">パラメーター - rename</span><span class="sxs-lookup"><span data-stu-id="a6996-183">Parameters - rename</span></span>

<span data-ttu-id="a6996-184">node</span><span class="sxs-lookup"><span data-stu-id="a6996-184">node</span></span>  

<!-- -->

<span data-ttu-id="a6996-185">newname</span><span class="sxs-lookup"><span data-stu-id="a6996-185">newname</span></span>  

### <a name="return-value---rename"></a><span data-ttu-id="a6996-186">戻り値 - rename</span><span class="sxs-lookup"><span data-stu-id="a6996-186">Return Value - rename</span></span>

## <a name="method-undocheckout"></a><span data-ttu-id="a6996-187">メソッド undoCheckOut</span><span class="sxs-lookup"><span data-stu-id="a6996-187">Method undoCheckOut</span></span>

```xpp
public boolean undoCheckOut(TreeNode node, [boolean showDialog])
```

### <a name="parameters---undocheckout"></a><span data-ttu-id="a6996-188">パラメーター - undoCheckOut</span><span class="sxs-lookup"><span data-stu-id="a6996-188">Parameters - undoCheckOut</span></span>

<span data-ttu-id="a6996-189">node</span><span class="sxs-lookup"><span data-stu-id="a6996-189">node</span></span>  

<!-- -->

<span data-ttu-id="a6996-190">showDialog</span><span class="sxs-lookup"><span data-stu-id="a6996-190">showDialog</span></span>  

### <a name="return-value---undocheckout"></a><span data-ttu-id="a6996-191">戻り値 - undoCheckOut</span><span class="sxs-lookup"><span data-stu-id="a6996-191">Return Value - undoCheckOut</span></span>

## <a name="method-unwantedobjecttypes"></a><span data-ttu-id="a6996-192">メソッド unwantedObjectTypes</span><span class="sxs-lookup"><span data-stu-id="a6996-192">Method unwantedObjectTypes</span></span>

```xpp
public Set unwantedObjectTypes()
```

### <a name="return-value---unwantedobjecttypes"></a><span data-ttu-id="a6996-193">戻り値 - unwantedObjectTypes</span><span class="sxs-lookup"><span data-stu-id="a6996-193">Return Value - unwantedObjectTypes</span></span>

## <a name="method-coloraot"></a><span data-ttu-id="a6996-194">メソッド colorAOT</span><span class="sxs-lookup"><span data-stu-id="a6996-194">Method colorAOT</span></span>

```xpp
public void colorAOT()
```

## <a name="method-save"></a><span data-ttu-id="a6996-195">メソッド save</span><span class="sxs-lookup"><span data-stu-id="a6996-195">Method save</span></span>

```xpp
public void save(TreeNode node)
```

### <a name="parameters---save"></a><span data-ttu-id="a6996-196">パラメーター - save</span><span class="sxs-lookup"><span data-stu-id="a6996-196">Parameters - save</span></span>

<span data-ttu-id="a6996-197">node</span><span class="sxs-lookup"><span data-stu-id="a6996-197">node</span></span>  

## <a name="method-showhistory"></a><span data-ttu-id="a6996-198">メソッド showHistory</span><span class="sxs-lookup"><span data-stu-id="a6996-198">Method showHistory</span></span>

```xpp
public void showHistory(TreeNode node)
```

### <a name="parameters---showhistory"></a><span data-ttu-id="a6996-199">パラメーター - showHistory</span><span class="sxs-lookup"><span data-stu-id="a6996-199">Parameters - showHistory</span></span>

<span data-ttu-id="a6996-200">node</span><span class="sxs-lookup"><span data-stu-id="a6996-200">node</span></span>  

## <a name="method-updatecheckedoutlist"></a><span data-ttu-id="a6996-201">メソッド updateCheckedOutList</span><span class="sxs-lookup"><span data-stu-id="a6996-201">Method updateCheckedOutList</span></span>

```xpp
public void updateCheckedOutList(Set checkedOutObjects)
```

### <a name="parameters---updatecheckedoutlist"></a><span data-ttu-id="a6996-202">パラメーター - updateCheckedOutList</span><span class="sxs-lookup"><span data-stu-id="a6996-202">Parameters - updateCheckedOutList</span></span>

<span data-ttu-id="a6996-203">checkedOutObjects</span><span class="sxs-lookup"><span data-stu-id="a6996-203">checkedOutObjects</span></span>  

## <a name="method-getlatestversion"></a><span data-ttu-id="a6996-204">メソッド getLatestVersion</span><span class="sxs-lookup"><span data-stu-id="a6996-204">Method getLatestVersion</span></span>

```xpp
public void getLatestVersion([TreeNode node], [boolean delLocalFiles])
```

### <a name="parameters---getlatestversion"></a><span data-ttu-id="a6996-205">パラメーター - getLatestVersion</span><span class="sxs-lookup"><span data-stu-id="a6996-205">Parameters - getLatestVersion</span></span>

<span data-ttu-id="a6996-206">node</span><span class="sxs-lookup"><span data-stu-id="a6996-206">node</span></span>  

<!-- -->

<span data-ttu-id="a6996-207">delLocalFiles</span><span class="sxs-lookup"><span data-stu-id="a6996-207">delLocalFiles</span></span>  

## <a name="method-checkin"></a><span data-ttu-id="a6996-208">メソッド checkIn</span><span class="sxs-lookup"><span data-stu-id="a6996-208">Method checkIn</span></span>

```xpp
public void checkIn(TreeNode node)
```

### <a name="parameters---checkin"></a><span data-ttu-id="a6996-209">パラメーター - checkIn</span><span class="sxs-lookup"><span data-stu-id="a6996-209">Parameters - checkIn</span></span>

<span data-ttu-id="a6996-210">node</span><span class="sxs-lookup"><span data-stu-id="a6996-210">node</span></span>  

## <a name="method-new"></a><span data-ttu-id="a6996-211">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a6996-211">Method new</span></span>

<span data-ttu-id="a6996-212">xVersionControl クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6996-212">Initializes a new instance of the xVersionControl class.</span></span>

```xpp
public void new()
```

## <a name="method-reload"></a><span data-ttu-id="a6996-213">メソッド reload</span><span class="sxs-lookup"><span data-stu-id="a6996-213">Method reload</span></span>

```xpp
public void reload()
```

## <a name="method-getlabelversion"></a><span data-ttu-id="a6996-214">メソッド getLabelVersion</span><span class="sxs-lookup"><span data-stu-id="a6996-214">Method getLabelVersion</span></span>

```xpp
public void getLabelVersion([TreeNode node], [str label])
```

### <a name="parameters---getlabelversion"></a><span data-ttu-id="a6996-215">パラメーター - getLabelVersion</span><span class="sxs-lookup"><span data-stu-id="a6996-215">Parameters - getLabelVersion</span></span>

<span data-ttu-id="a6996-216">node</span><span class="sxs-lookup"><span data-stu-id="a6996-216">node</span></span>  

<!-- -->

<span data-ttu-id="a6996-217">ラベル</span><span class="sxs-lookup"><span data-stu-id="a6996-217">label</span></span>  



