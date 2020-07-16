---
title: VSProjectsNode クラス
description: このトピックでは、VSProjectsNode クラスについて説明します。
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
ms.openlocfilehash: a736eab152ed5be142e9e8682cae584629fd2a3a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502779"
---
# <a name="class-vsprojectsnode"></a><span data-ttu-id="f2ce6-103">クラス VSProjectsNode</span><span class="sxs-lookup"><span data-stu-id="f2ce6-103">Class VSProjectsNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectsNode extends xResourceNode
```

<span data-ttu-id="f2ce6-104">VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードのルートです。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-104">The VSProjectNode class is the root of the Microsoft Visual Studio project nodes in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ce6-105">備考</span><span class="sxs-lookup"><span data-stu-id="f2ce6-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f2ce6-106">例</span><span class="sxs-lookup"><span data-stu-id="f2ce6-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f2ce6-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="f2ce6-107">Methods</span></span>

| <span data-ttu-id="f2ce6-108">方法</span><span class="sxs-lookup"><span data-stu-id="f2ce6-108">Method</span></span>                                                                                            | <span data-ttu-id="f2ce6-109">説明</span><span class="sxs-lookup"><span data-stu-id="f2ce6-109">Description</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ce6-110">public TreeNode AOTfindChild(str name, \[int nodeType\])</span><span class="sxs-lookup"><span data-stu-id="f2ce6-110">public TreeNode AOTfindChild(str name, \[int nodeType\])</span></span>                                          | <span data-ttu-id="f2ce6-111">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-111">Finds the specified child node of this node.</span></span>                                               |
| <span data-ttu-id="f2ce6-112">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span><span class="sxs-lookup"><span data-stu-id="f2ce6-112">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span></span> | <span data-ttu-id="f2ce6-113">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-113">Creates a new instance of the VSProjectNode class.</span></span>                                         |
| <span data-ttu-id="f2ce6-114">public container getProjectsDeployingTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="f2ce6-114">public container getProjectsDeployingTo(DeployTo deployTo)</span></span>                                        | <span data-ttu-id="f2ce6-115">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-115">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>            |
| <span data-ttu-id="f2ce6-116">public container getProjectsModifiedAfter(DateTime timestamp)</span><span class="sxs-lookup"><span data-stu-id="f2ce6-116">public container getProjectsModifiedAfter(DateTime timestamp)</span></span>                                     | <span data-ttu-id="f2ce6-117">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-117">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span> |
| <span data-ttu-id="f2ce6-118">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span><span class="sxs-lookup"><span data-stu-id="f2ce6-118">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span></span>                              |                                                                                            |
| <span data-ttu-id="f2ce6-119">public Object getVSProjectNodeObservable()</span><span class="sxs-lookup"><span data-stu-id="f2ce6-119">public Object getVSProjectNodeObservable()</span></span>                                                        | <span data-ttu-id="f2ce6-120">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-120">Gets the VSProjectNodeObservable object.</span></span>                                                   |
| <span data-ttu-id="f2ce6-121">public void AOTrefresh()</span><span class="sxs-lookup"><span data-stu-id="f2ce6-121">public void AOTrefresh()</span></span>                                                                          | <span data-ttu-id="f2ce6-122">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-122">Updates the node with the latest changes to the .aod file.</span></span>                                 |

## <a name="method-aotfindchild"></a><span data-ttu-id="f2ce6-123">メソッド AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="f2ce6-123">Method AOTfindChild</span></span>

<span data-ttu-id="f2ce6-124">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-124">Finds the specified child node of this node.</span></span>

```xpp
public TreeNode AOTfindChild(str name, [int nodeType])
```

### <a name="parameters---aotfindchild"></a><span data-ttu-id="f2ce6-125">パラメーター - AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="f2ce6-125">Parameters - AOTfindChild</span></span>

<span data-ttu-id="f2ce6-126">名前</span><span class="sxs-lookup"><span data-stu-id="f2ce6-126">name</span></span>  

<!-- -->

<span data-ttu-id="f2ce6-127">nodeType</span><span class="sxs-lookup"><span data-stu-id="f2ce6-127">nodeType</span></span>  

### <a name="return-value---aotfindchild"></a><span data-ttu-id="f2ce6-128">戻り値 - AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="f2ce6-128">Return Value - AOTfindChild</span></span>

<span data-ttu-id="f2ce6-129">指定したツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-129">The specified tree node.</span></span>

## <a name="method-createprojectnode"></a><span data-ttu-id="f2ce6-130">メソッド createProjectNode</span><span class="sxs-lookup"><span data-stu-id="f2ce6-130">Method createProjectNode</span></span>

<span data-ttu-id="f2ce6-131">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-131">Creates a new instance of the VSProjectNode class.</span></span>

```xpp
public VSProjectNode createProjectNode(str name, str projectTypesString, [boolean virtualNode])
```

### <a name="parameters---createprojectnode"></a><span data-ttu-id="f2ce6-132">パラメーター - createProjectNode</span><span class="sxs-lookup"><span data-stu-id="f2ce6-132">Parameters - createProjectNode</span></span>

<span data-ttu-id="f2ce6-133">名前</span><span class="sxs-lookup"><span data-stu-id="f2ce6-133">name</span></span>  
<span data-ttu-id="f2ce6-134">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-134">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="f2ce6-135">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-135">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="f2ce6-136">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="f2ce6-136">projectTypesString</span></span>  
<span data-ttu-id="f2ce6-137">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-137">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="f2ce6-138">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-138">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="f2ce6-139">virtualNode</span><span class="sxs-lookup"><span data-stu-id="f2ce6-139">virtualNode</span></span>  
<span data-ttu-id="f2ce6-140">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-140">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="f2ce6-141">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-141">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

### <a name="return-value---createprojectnode"></a><span data-ttu-id="f2ce6-142">戻り値 - createProjectNode</span><span class="sxs-lookup"><span data-stu-id="f2ce6-142">Return Value - createProjectNode</span></span>

<span data-ttu-id="f2ce6-143">作成された VSProjectNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-143">The VSProjectNode object that is created.</span></span>

## <a name="method-getprojectsdeployingto"></a><span data-ttu-id="f2ce6-144">メソッド getProjectsDeployingTo</span><span class="sxs-lookup"><span data-stu-id="f2ce6-144">Method getProjectsDeployingTo</span></span>

<span data-ttu-id="f2ce6-145">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-145">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>

```xpp
public container getProjectsDeployingTo(DeployTo deployTo)
```

### <a name="parameters---getprojectsdeployingto"></a><span data-ttu-id="f2ce6-146">パラメーター - getProjectsDeployingTo</span><span class="sxs-lookup"><span data-stu-id="f2ce6-146">Parameters - getProjectsDeployingTo</span></span>

<span data-ttu-id="f2ce6-147">deployTo</span><span class="sxs-lookup"><span data-stu-id="f2ce6-147">deployTo</span></span>  
<span data-ttu-id="f2ce6-148">deployTo プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-148">The value of the deployTo property.</span></span>

### <a name="return-value---getprojectsdeployingto"></a><span data-ttu-id="f2ce6-149">戻り値 - getProjectsDeployingTo</span><span class="sxs-lookup"><span data-stu-id="f2ce6-149">Return Value - getProjectsDeployingTo</span></span>

<span data-ttu-id="f2ce6-150">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-150">A list of VSProjectNode objects.</span></span>

## <a name="method-getprojectsmodifiedafter"></a><span data-ttu-id="f2ce6-151">メソッド getProjectsModifiedAfter</span><span class="sxs-lookup"><span data-stu-id="f2ce6-151">Method getProjectsModifiedAfter</span></span>

<span data-ttu-id="f2ce6-152">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-152">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span>

```xpp
public container getProjectsModifiedAfter(DateTime timestamp)
```

### <a name="parameters---getprojectsmodifiedafter"></a><span data-ttu-id="f2ce6-153">パラメーター - getProjectsModifiedAfter</span><span class="sxs-lookup"><span data-stu-id="f2ce6-153">Parameters - getProjectsModifiedAfter</span></span>

<span data-ttu-id="f2ce6-154">timestamp</span><span class="sxs-lookup"><span data-stu-id="f2ce6-154">timestamp</span></span>  
<span data-ttu-id="f2ce6-155">DB\_DATETIME\_TYPE 値としての日時。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-155">The date and time as a DB\_DATETIME\_TYPE value.</span></span>

### <a name="return-value---getprojectsmodifiedafter"></a><span data-ttu-id="f2ce6-156">戻り値 - getProjectsModifiedAfter</span><span class="sxs-lookup"><span data-stu-id="f2ce6-156">Return Value - getProjectsModifiedAfter</span></span>

<span data-ttu-id="f2ce6-157">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-157">A list of VSProjectNode objects.</span></span>

## <a name="method-gettypenodefromguid"></a><span data-ttu-id="f2ce6-158">メソッド getTypeNodeFromGuid</span><span class="sxs-lookup"><span data-stu-id="f2ce6-158">Method getTypeNodeFromGuid</span></span>

```xpp
public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)
```

### <a name="parameters---gettypenodefromguid"></a><span data-ttu-id="f2ce6-159">パラメーター - getTypeNodeFromGuid</span><span class="sxs-lookup"><span data-stu-id="f2ce6-159">Parameters - getTypeNodeFromGuid</span></span>

<span data-ttu-id="f2ce6-160">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="f2ce6-160">projectTypesString</span></span>  

### <a name="return-value---gettypenodefromguid"></a><span data-ttu-id="f2ce6-161">戻り値 - getTypeNodeFromGuid</span><span class="sxs-lookup"><span data-stu-id="f2ce6-161">Return Value - getTypeNodeFromGuid</span></span>

## <a name="method-getvsprojectnodeobservable"></a><span data-ttu-id="f2ce6-162">メソッド getVSProjectNodeObservable</span><span class="sxs-lookup"><span data-stu-id="f2ce6-162">Method getVSProjectNodeObservable</span></span>

<span data-ttu-id="f2ce6-163">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-163">Gets the VSProjectNodeObservable object.</span></span>

```xpp
public Object getVSProjectNodeObservable()
```

### <a name="return-value---getvsprojectnodeobservable"></a><span data-ttu-id="f2ce6-164">戻り値 - getVSProjectNodeObservable</span><span class="sxs-lookup"><span data-stu-id="f2ce6-164">Return Value - getVSProjectNodeObservable</span></span>

<span data-ttu-id="f2ce6-165">VSProjectNodeObservable オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-165">The VSProjectNodeObservable object.</span></span>

### <a name="remarks---getvsprojectnodeobservable"></a><span data-ttu-id="f2ce6-166">備考 - getVSProjectNodeObservable</span><span class="sxs-lookup"><span data-stu-id="f2ce6-166">Remarks - getVSProjectNodeObservable</span></span>

<span data-ttu-id="f2ce6-167">オブザーバーはこれで登録でき、Visual Studio プロジェクトで CRUD 操作の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-167">Observers can register with this and get notified of CRUD operations on Visual Studio projects.</span></span>

## <a name="method-aotrefresh"></a><span data-ttu-id="f2ce6-168">メソッド AOTrefresh</span><span class="sxs-lookup"><span data-stu-id="f2ce6-168">Method AOTrefresh</span></span>

<span data-ttu-id="f2ce6-169">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="f2ce6-169">Updates the node with the latest changes to the .aod file.</span></span>

```xpp
public void AOTrefresh()
```

