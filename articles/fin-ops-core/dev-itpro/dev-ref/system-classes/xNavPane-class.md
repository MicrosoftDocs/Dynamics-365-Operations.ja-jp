---
title: xNavPane クラス
description: このトピックでは、xNavPane クラスについて説明します。
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
ms.openlocfilehash: c389b0dcbbbabbe21c2accfc0f37cb610f1e0d23
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502678"
---
# <a name="class-xnavpane"></a><span data-ttu-id="7d1a3-103">クラス xNavPane</span><span class="sxs-lookup"><span data-stu-id="7d1a3-103">Class xNavPane</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xNavPane extends Object
```

## <a name="remarks"></a><span data-ttu-id="7d1a3-104">備考</span><span class="sxs-lookup"><span data-stu-id="7d1a3-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7d1a3-105">例</span><span class="sxs-lookup"><span data-stu-id="7d1a3-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7d1a3-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7d1a3-106">Methods</span></span>

| <span data-ttu-id="7d1a3-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d1a3-107">Method</span></span>                                                                                                | <span data-ttu-id="7d1a3-108">説明</span><span class="sxs-lookup"><span data-stu-id="7d1a3-108">Description</span></span>                                       |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7d1a3-109">public boolean collapseFavoriteNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-109">public boolean collapseFavoriteNode(str path)</span></span>                                                         |                                                   |
| <span data-ttu-id="7d1a3-110">public boolean collapseNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-110">public boolean collapseNode(str path)</span></span>                                                                 |                                                   |
| <span data-ttu-id="7d1a3-111">public boolean expandFavoriteNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-111">public boolean expandFavoriteNode(str path)</span></span>                                                           |                                                   |
| <span data-ttu-id="7d1a3-112">public boolean expandNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-112">public boolean expandNode(str path)</span></span>                                                                   |                                                   |
| <span data-ttu-id="7d1a3-113">public boolean favPaneVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d1a3-113">public boolean favPaneVisible(\[boolean value\])</span></span>                                                      |                                                   |
| <span data-ttu-id="7d1a3-114">public container getButtons()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-114">public container getButtons()</span></span>                                                                         |                                                   |
| <span data-ttu-id="7d1a3-115">public str getCurrMenuName()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-115">public str getCurrMenuName()</span></span>                                                                          |                                                   |
| <span data-ttu-id="7d1a3-116">public TreeNode getSelectedFavoriteNode()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-116">public TreeNode getSelectedFavoriteNode()</span></span>                                                             |                                                   |
| <span data-ttu-id="7d1a3-117">public TreeNode getSelectedNode()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-117">public TreeNode getSelectedNode()</span></span>                                                                     |                                                   |
| <span data-ttu-id="7d1a3-118">public boolean navPaneVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7d1a3-118">public boolean navPaneVisible(\[boolean value\])</span></span>                                                      |                                                   |
| <span data-ttu-id="7d1a3-119">public boolean runFavoriteNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-119">public boolean runFavoriteNode(str path)</span></span>                                                              |                                                   |
| <span data-ttu-id="7d1a3-120">public boolean runNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-120">public boolean runNode(str path)</span></span>                                                                      |                                                   |
| <span data-ttu-id="7d1a3-121">public str selectedFavoriteGroup(\[str groupName\])</span><span class="sxs-lookup"><span data-stu-id="7d1a3-121">public str selectedFavoriteGroup(\[str groupName\])</span></span>                                                   |                                                   |
| <span data-ttu-id="7d1a3-122">public str selectedGroup(\[str groupName\])</span><span class="sxs-lookup"><span data-stu-id="7d1a3-122">public str selectedGroup(\[str groupName\])</span></span>                                                           |                                                   |
| <span data-ttu-id="7d1a3-123">public boolean setSelectedFavoriteNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-123">public boolean setSelectedFavoriteNode(str path)</span></span>                                                      |                                                   |
| <span data-ttu-id="7d1a3-124">public boolean setSelectedNode(str path)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-124">public boolean setSelectedNode(str path)</span></span>                                                              |                                                   |
| <span data-ttu-id="7d1a3-125">public void refreshFavorites(\[str selectFavoriteGroup\], \[int workspaceNum\], \[boolean saveToDB\])</span><span class="sxs-lookup"><span data-stu-id="7d1a3-125">public void refreshFavorites(\[str selectFavoriteGroup\], \[int workspaceNum\], \[boolean saveToDB\])</span></span> |                                                   |
| <span data-ttu-id="7d1a3-126">public void setCurrMenuButtons(container buttons)</span><span class="sxs-lookup"><span data-stu-id="7d1a3-126">public void setCurrMenuButtons(container buttons)</span></span>                                                     |                                                   |
| <span data-ttu-id="7d1a3-127">public void loadStartupButtons()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-127">public void loadStartupButtons()</span></span>                                                                      |                                                   |
| <span data-ttu-id="7d1a3-128">public void new()</span><span class="sxs-lookup"><span data-stu-id="7d1a3-128">public void new()</span></span>                                                                                     | <span data-ttu-id="7d1a3-129">xNavPane クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7d1a3-129">Initializes a new instance of the xNavPane class.</span></span> |

## <a name="method-collapsefavoritenode"></a><span data-ttu-id="7d1a3-130">メソッド collapseFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-130">Method collapseFavoriteNode</span></span>

```xpp
public boolean collapseFavoriteNode(str path)
```

### <a name="parameters---collapsefavoritenode"></a><span data-ttu-id="7d1a3-131">パラメーター - collapseFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-131">Parameters - collapseFavoriteNode</span></span>

<span data-ttu-id="7d1a3-132">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-132">path</span></span>  

### <a name="return-value---collapsefavoritenode"></a><span data-ttu-id="7d1a3-133">戻り値 - collapseFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-133">Return Value - collapseFavoriteNode</span></span>

## <a name="method-collapsenode"></a><span data-ttu-id="7d1a3-134">メソッド collapseNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-134">Method collapseNode</span></span>

```xpp
public boolean collapseNode(str path)
```

### <a name="parameters---collapsenode"></a><span data-ttu-id="7d1a3-135">パラメーター - collapseNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-135">Parameters - collapseNode</span></span>

<span data-ttu-id="7d1a3-136">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-136">path</span></span>  

### <a name="return-value---collapsenode"></a><span data-ttu-id="7d1a3-137">戻り値 - collapseNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-137">Return Value - collapseNode</span></span>

## <a name="method-expandfavoritenode"></a><span data-ttu-id="7d1a3-138">メソッド expandFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-138">Method expandFavoriteNode</span></span>

```xpp
public boolean expandFavoriteNode(str path)
```

### <a name="parameters---expandfavoritenode"></a><span data-ttu-id="7d1a3-139">パラメーター - expandFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-139">Parameters - expandFavoriteNode</span></span>

<span data-ttu-id="7d1a3-140">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-140">path</span></span>  

### <a name="return-value---expandfavoritenode"></a><span data-ttu-id="7d1a3-141">戻り値 - expandFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-141">Return Value - expandFavoriteNode</span></span>

## <a name="method-expandnode"></a><span data-ttu-id="7d1a3-142">メソッド expandNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-142">Method expandNode</span></span>

```xpp
public boolean expandNode(str path)
```

### <a name="parameters---expandnode"></a><span data-ttu-id="7d1a3-143">パラメーター - expandNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-143">Parameters - expandNode</span></span>

<span data-ttu-id="7d1a3-144">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-144">path</span></span>  

### <a name="return-value---expandnode"></a><span data-ttu-id="7d1a3-145">戻り値 - expandNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-145">Return Value - expandNode</span></span>

## <a name="method-favpanevisible"></a><span data-ttu-id="7d1a3-146">メソッド favPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-146">Method favPaneVisible</span></span>

```xpp
public boolean favPaneVisible([boolean value])
```

### <a name="parameters---favpanevisible"></a><span data-ttu-id="7d1a3-147">パラメーター - favPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-147">Parameters - favPaneVisible</span></span>

<span data-ttu-id="7d1a3-148">値</span><span class="sxs-lookup"><span data-stu-id="7d1a3-148">value</span></span>  

### <a name="return-value---favpanevisible"></a><span data-ttu-id="7d1a3-149">戻り値 - favPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-149">Return Value - favPaneVisible</span></span>

## <a name="method-getbuttons"></a><span data-ttu-id="7d1a3-150">メソッド getButtons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-150">Method getButtons</span></span>

```xpp
public container getButtons()
```

### <a name="return-value---getbuttons"></a><span data-ttu-id="7d1a3-151">戻り値 - getButtons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-151">Return Value - getButtons</span></span>

## <a name="method-getcurrmenuname"></a><span data-ttu-id="7d1a3-152">メソッド getCurrMenuName</span><span class="sxs-lookup"><span data-stu-id="7d1a3-152">Method getCurrMenuName</span></span>

```xpp
public str getCurrMenuName()
```

### <a name="return-value---getcurrmenuname"></a><span data-ttu-id="7d1a3-153">戻り値 - getCurrMenuName</span><span class="sxs-lookup"><span data-stu-id="7d1a3-153">Return Value - getCurrMenuName</span></span>

## <a name="method-getselectedfavoritenode"></a><span data-ttu-id="7d1a3-154">メソッド getSelectedFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-154">Method getSelectedFavoriteNode</span></span>

```xpp
public TreeNode getSelectedFavoriteNode()
```

### <a name="return-value---getselectedfavoritenode"></a><span data-ttu-id="7d1a3-155">戻り値 - getSelectedFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-155">Return Value - getSelectedFavoriteNode</span></span>

## <a name="method-getselectednode"></a><span data-ttu-id="7d1a3-156">メソッド getSelectedNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-156">Method getSelectedNode</span></span>

```xpp
public TreeNode getSelectedNode()
```

### <a name="return-value---getselectednode"></a><span data-ttu-id="7d1a3-157">戻り値 - getSelectedNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-157">Return Value - getSelectedNode</span></span>

## <a name="method-navpanevisible"></a><span data-ttu-id="7d1a3-158">メソッド navPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-158">Method navPaneVisible</span></span>

```xpp
public boolean navPaneVisible([boolean value])
```

### <a name="parameters---navpanevisible"></a><span data-ttu-id="7d1a3-159">パラメーター - navPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-159">Parameters - navPaneVisible</span></span>

<span data-ttu-id="7d1a3-160">値</span><span class="sxs-lookup"><span data-stu-id="7d1a3-160">value</span></span>  

### <a name="return-value---navpanevisible"></a><span data-ttu-id="7d1a3-161">戻り値 - navPaneVisible</span><span class="sxs-lookup"><span data-stu-id="7d1a3-161">Return Value - navPaneVisible</span></span>

## <a name="method-runfavoritenode"></a><span data-ttu-id="7d1a3-162">メソッド runFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-162">Method runFavoriteNode</span></span>

```xpp
public boolean runFavoriteNode(str path)
```

### <a name="parameters---runfavoritenode"></a><span data-ttu-id="7d1a3-163">パラメーター - runFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-163">Parameters - runFavoriteNode</span></span>

<span data-ttu-id="7d1a3-164">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-164">path</span></span>  

### <a name="return-value---runfavoritenode"></a><span data-ttu-id="7d1a3-165">戻り値 - runFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-165">Return Value - runFavoriteNode</span></span>

## <a name="method-runnode"></a><span data-ttu-id="7d1a3-166">メソッド runNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-166">Method runNode</span></span>

```xpp
public boolean runNode(str path)
```

### <a name="parameters---runnode"></a><span data-ttu-id="7d1a3-167">パラメーター - runNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-167">Parameters - runNode</span></span>

<span data-ttu-id="7d1a3-168">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-168">path</span></span>  

### <a name="return-value---runnode"></a><span data-ttu-id="7d1a3-169">戻り値 - runNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-169">Return Value - runNode</span></span>

## <a name="method-selectedfavoritegroup"></a><span data-ttu-id="7d1a3-170">メソッド selectedFavoriteGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-170">Method selectedFavoriteGroup</span></span>

```xpp
public str selectedFavoriteGroup([str groupName])
```

### <a name="parameters---selectedfavoritegroup"></a><span data-ttu-id="7d1a3-171">パラメーター - selectedFavoriteGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-171">Parameters - selectedFavoriteGroup</span></span>

<span data-ttu-id="7d1a3-172">groupName</span><span class="sxs-lookup"><span data-stu-id="7d1a3-172">groupName</span></span>  

### <a name="return-value---selectedfavoritegroup"></a><span data-ttu-id="7d1a3-173">戻り値 - selectedFavoriteGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-173">Return Value - selectedFavoriteGroup</span></span>

## <a name="method-selectedgroup"></a><span data-ttu-id="7d1a3-174">メソッド selectedGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-174">Method selectedGroup</span></span>

```xpp
public str selectedGroup([str groupName])
```

### <a name="parameters---selectedgroup"></a><span data-ttu-id="7d1a3-175">パラメーター - selectedGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-175">Parameters - selectedGroup</span></span>

<span data-ttu-id="7d1a3-176">groupName</span><span class="sxs-lookup"><span data-stu-id="7d1a3-176">groupName</span></span>  

### <a name="return-value---selectedgroup"></a><span data-ttu-id="7d1a3-177">戻り値 - selectedGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-177">Return Value - selectedGroup</span></span>

## <a name="method-setselectedfavoritenode"></a><span data-ttu-id="7d1a3-178">メソッド setSelectedFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-178">Method setSelectedFavoriteNode</span></span>

```xpp
public boolean setSelectedFavoriteNode(str path)
```

### <a name="parameters---setselectedfavoritenode"></a><span data-ttu-id="7d1a3-179">パラメーター - setSelectedFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-179">Parameters - setSelectedFavoriteNode</span></span>

<span data-ttu-id="7d1a3-180">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-180">path</span></span>  

### <a name="return-value---setselectedfavoritenode"></a><span data-ttu-id="7d1a3-181">戻り値 - setSelectedFavoriteNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-181">Return Value - setSelectedFavoriteNode</span></span>

## <a name="method-setselectednode"></a><span data-ttu-id="7d1a3-182">メソッド setSelectedNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-182">Method setSelectedNode</span></span>

```xpp
public boolean setSelectedNode(str path)
```

### <a name="parameters---setselectednode"></a><span data-ttu-id="7d1a3-183">パラメーター - setSelectedNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-183">Parameters - setSelectedNode</span></span>

<span data-ttu-id="7d1a3-184">path</span><span class="sxs-lookup"><span data-stu-id="7d1a3-184">path</span></span>  

### <a name="return-value---setselectednode"></a><span data-ttu-id="7d1a3-185">戻り値 - setSelectedNode</span><span class="sxs-lookup"><span data-stu-id="7d1a3-185">Return Value - setSelectedNode</span></span>

## <a name="method-refreshfavorites"></a><span data-ttu-id="7d1a3-186">メソッド refreshFavorites</span><span class="sxs-lookup"><span data-stu-id="7d1a3-186">Method refreshFavorites</span></span>

```xpp
public void refreshFavorites([str selectFavoriteGroup], [int workspaceNum], [boolean saveToDB])
```

### <a name="parameters---refreshfavorites"></a><span data-ttu-id="7d1a3-187">パラメーター - refreshFavorites</span><span class="sxs-lookup"><span data-stu-id="7d1a3-187">Parameters - refreshFavorites</span></span>

<span data-ttu-id="7d1a3-188">selectFavoriteGroup</span><span class="sxs-lookup"><span data-stu-id="7d1a3-188">selectFavoriteGroup</span></span>  

<!-- -->

<span data-ttu-id="7d1a3-189">workspaceNum</span><span class="sxs-lookup"><span data-stu-id="7d1a3-189">workspaceNum</span></span>  

<!-- -->

<span data-ttu-id="7d1a3-190">saveToDB</span><span class="sxs-lookup"><span data-stu-id="7d1a3-190">saveToDB</span></span>  

## <a name="method-setcurrmenubuttons"></a><span data-ttu-id="7d1a3-191">メソッド setCurrMenuButtons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-191">Method setCurrMenuButtons</span></span>

```xpp
public void setCurrMenuButtons(container buttons)
```

### <a name="parameters---setcurrmenubuttons"></a><span data-ttu-id="7d1a3-192">パラメーター - setCurrMenuButtons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-192">Parameters - setCurrMenuButtons</span></span>

<span data-ttu-id="7d1a3-193">buttons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-193">buttons</span></span>  

## <a name="method-loadstartupbuttons"></a><span data-ttu-id="7d1a3-194">メソッド loadStartupButtons</span><span class="sxs-lookup"><span data-stu-id="7d1a3-194">Method loadStartupButtons</span></span>

```xpp
public void loadStartupButtons()
```

## <a name="method-new"></a><span data-ttu-id="7d1a3-195">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7d1a3-195">Method new</span></span>

<span data-ttu-id="7d1a3-196">xNavPane クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7d1a3-196">Initializes a new instance of the xNavPane class.</span></span>

```xpp
public void new()
```

