---
title: VSProjectNode クラス
description: このトピックでは、VSProjectNode クラスについて説明します。
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
ms.openlocfilehash: 5f80602b19a9cf2f2489000d8c2ee3bbf9d24cf8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502693"
---
# <a name="class-vsprojectnode"></a><span data-ttu-id="84bce-103">クラス VSProjectNode</span><span class="sxs-lookup"><span data-stu-id="84bce-103">Class VSProjectNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectNode extends xResourceNode
```

<span data-ttu-id="84bce-104">VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでプロジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="84bce-104">The VSProjectNode class represents projects in the Microsoft Visual Studio project nodes in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="84bce-105">備考</span><span class="sxs-lookup"><span data-stu-id="84bce-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="84bce-106">例</span><span class="sxs-lookup"><span data-stu-id="84bce-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="84bce-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="84bce-107">Methods</span></span>

| <span data-ttu-id="84bce-108">方法</span><span class="sxs-lookup"><span data-stu-id="84bce-108">Method</span></span>                                                                | <span data-ttu-id="84bce-109">説明</span><span class="sxs-lookup"><span data-stu-id="84bce-109">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84bce-110">public container extract(\[str path\], \[boolean extractReferenced\])</span><span class="sxs-lookup"><span data-stu-id="84bce-110">public container extract(\[str path\], \[boolean extractReferenced\])</span></span> | <span data-ttu-id="84bce-111">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="84bce-111">Extracts the whole project to disk.</span></span>                                                               |
| <span data-ttu-id="84bce-112">public VSProjectFolderNode getContentNode()</span><span class="sxs-lookup"><span data-stu-id="84bce-112">public VSProjectFolderNode getContentNode()</span></span>                           | <span data-ttu-id="84bce-113">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-113">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>        |
| <span data-ttu-id="84bce-114">public DeployTo getDeployTo()</span><span class="sxs-lookup"><span data-stu-id="84bce-114">public DeployTo getDeployTo()</span></span>                                         | <span data-ttu-id="84bce-115">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-115">Gets value of the deployTo property.</span></span>                                                              |
| <span data-ttu-id="84bce-116">public VSProjectFolderNode getOutputNode()</span><span class="sxs-lookup"><span data-stu-id="84bce-116">public VSProjectFolderNode getOutputNode()</span></span>                            | <span data-ttu-id="84bce-117">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-117">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>  |
| <span data-ttu-id="84bce-118">public VSProjectFileNode getPrimaryOutputNode()</span><span class="sxs-lookup"><span data-stu-id="84bce-118">public VSProjectFileNode getPrimaryOutputNode()</span></span>                       | <span data-ttu-id="84bce-119">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-119">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span> |
| <span data-ttu-id="84bce-120">public str getPrimaryTargetFileName()</span><span class="sxs-lookup"><span data-stu-id="84bce-120">public str getPrimaryTargetFileName()</span></span>                                 | <span data-ttu-id="84bce-121">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-121">Gets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="84bce-122">public Map getProxies()</span><span class="sxs-lookup"><span data-stu-id="84bce-122">public Map getProxies()</span></span>                                               | <span data-ttu-id="84bce-123">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-123">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="84bce-124">public container getProxiesContainer()</span><span class="sxs-lookup"><span data-stu-id="84bce-124">public container getProxiesContainer()</span></span>                                | <span data-ttu-id="84bce-125">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-125">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="84bce-126">public str getReferencedProjectsInAOT()</span><span class="sxs-lookup"><span data-stu-id="84bce-126">public str getReferencedProjectsInAOT()</span></span>                               | <span data-ttu-id="84bce-127">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-127">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>             |
| <span data-ttu-id="84bce-128">public str referencedProjects(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="84bce-128">public str referencedProjects(\[str value\])</span></span>                          |                                                                                                   |
| <span data-ttu-id="84bce-129">public void setPrimaryTargetFileName(str targetFileName)</span><span class="sxs-lookup"><span data-stu-id="84bce-129">public void setPrimaryTargetFileName(str targetFileName)</span></span>              | <span data-ttu-id="84bce-130">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="84bce-130">Sets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="84bce-131">public void extractToSpecificDir(str directory)</span><span class="sxs-lookup"><span data-stu-id="84bce-131">public void extractToSpecificDir(str directory)</span></span>                       |                                                                                                   |
| <span data-ttu-id="84bce-132">public void setDeployTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="84bce-132">public void setDeployTo(DeployTo deployTo)</span></span>                            | <span data-ttu-id="84bce-133">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="84bce-133">Sets the value of the deployTo property.</span></span>                                                          |

## <a name="method-extract"></a><span data-ttu-id="84bce-134">メソッド extract</span><span class="sxs-lookup"><span data-stu-id="84bce-134">Method extract</span></span>

<span data-ttu-id="84bce-135">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="84bce-135">Extracts the whole project to disk.</span></span>

```xpp
public container extract([str path], [boolean extractReferenced])
```

### <a name="parameters---extract"></a><span data-ttu-id="84bce-136">パラメーター - extract</span><span class="sxs-lookup"><span data-stu-id="84bce-136">Parameters - extract</span></span>

<span data-ttu-id="84bce-137">path</span><span class="sxs-lookup"><span data-stu-id="84bce-137">path</span></span>  
<span data-ttu-id="84bce-138">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="84bce-138">A Boolean value that determines whether to extract the referenced projects.</span></span>

<!-- -->

<span data-ttu-id="84bce-139">extractReferenced</span><span class="sxs-lookup"><span data-stu-id="84bce-139">extractReferenced</span></span>  
<span data-ttu-id="84bce-140">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="84bce-140">A Boolean value that determines whether to extract the referenced projects.</span></span>

### <a name="return-value---extract"></a><span data-ttu-id="84bce-141">戻り値 - extract</span><span class="sxs-lookup"><span data-stu-id="84bce-141">Return Value - extract</span></span>

<span data-ttu-id="84bce-142">プロジェクトの展開先のパスの一覧。</span><span class="sxs-lookup"><span data-stu-id="84bce-142">A list of paths where the project was extracted.</span></span>

## <a name="method-getcontentnode"></a><span data-ttu-id="84bce-143">メソッド getContentNode</span><span class="sxs-lookup"><span data-stu-id="84bce-143">Method getContentNode</span></span>

<span data-ttu-id="84bce-144">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-144">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

```xpp
public VSProjectFolderNode getContentNode()
```

### <a name="return-value---getcontentnode"></a><span data-ttu-id="84bce-145">戻り値 - getContentNode</span><span class="sxs-lookup"><span data-stu-id="84bce-145">Return Value - getContentNode</span></span>

<span data-ttu-id="84bce-146">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="84bce-146">The content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

## <a name="method-getdeployto"></a><span data-ttu-id="84bce-147">メソッド getDeployTo</span><span class="sxs-lookup"><span data-stu-id="84bce-147">Method getDeployTo</span></span>

<span data-ttu-id="84bce-148">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-148">Gets value of the deployTo property.</span></span>

```xpp
public DeployTo getDeployTo()
```

### <a name="return-value---getdeployto"></a><span data-ttu-id="84bce-149">戻り値 - getDeployTo</span><span class="sxs-lookup"><span data-stu-id="84bce-149">Return Value - getDeployTo</span></span>

<span data-ttu-id="84bce-150">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="84bce-150">The deployTo property value.</span></span>

## <a name="method-getoutputnode"></a><span data-ttu-id="84bce-151">メソッド getOutputNode</span><span class="sxs-lookup"><span data-stu-id="84bce-151">Method getOutputNode</span></span>

<span data-ttu-id="84bce-152">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-152">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

```xpp
public VSProjectFolderNode getOutputNode()
```

### <a name="return-value---getoutputnode"></a><span data-ttu-id="84bce-153">戻り値 - getOutputNode</span><span class="sxs-lookup"><span data-stu-id="84bce-153">Return Value - getOutputNode</span></span>

<span data-ttu-id="84bce-154">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="84bce-154">The output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

## <a name="method-getprimaryoutputnode"></a><span data-ttu-id="84bce-155">メソッド getPrimaryOutputNode</span><span class="sxs-lookup"><span data-stu-id="84bce-155">Method getPrimaryOutputNode</span></span>

<span data-ttu-id="84bce-156">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-156">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

```xpp
public VSProjectFileNode getPrimaryOutputNode()
```

### <a name="return-value---getprimaryoutputnode"></a><span data-ttu-id="84bce-157">戻り値 - getPrimaryOutputNode</span><span class="sxs-lookup"><span data-stu-id="84bce-157">Return Value - getPrimaryOutputNode</span></span>

<span data-ttu-id="84bce-158">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="84bce-158">A VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

## <a name="method-getprimarytargetfilename"></a><span data-ttu-id="84bce-159">メソッド getPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="84bce-159">Method getPrimaryTargetFileName</span></span>

<span data-ttu-id="84bce-160">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-160">Gets the primary target file name of the Visual Studio project.</span></span>

```xpp
public str getPrimaryTargetFileName()
```

### <a name="return-value---getprimarytargetfilename"></a><span data-ttu-id="84bce-161">戻り値 - getPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="84bce-161">Return Value - getPrimaryTargetFileName</span></span>

<span data-ttu-id="84bce-162">Visual Studio プロジェクトのプライマリ ターゲット ファイル名。</span><span class="sxs-lookup"><span data-stu-id="84bce-162">The primary target file name of the Visual Studio project.</span></span>

## <a name="method-getproxies"></a><span data-ttu-id="84bce-163">メソッド getProxies</span><span class="sxs-lookup"><span data-stu-id="84bce-163">Method getProxies</span></span>

<span data-ttu-id="84bce-164">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-164">Gets the proxies in this project.</span></span>

```xpp
public Map getProxies()
```

### <a name="return-value---getproxies"></a><span data-ttu-id="84bce-165">戻り値 - getProxies</span><span class="sxs-lookup"><span data-stu-id="84bce-165">Return Value - getProxies</span></span>

<span data-ttu-id="84bce-166">クラス、列挙、およびテーブルのキーを含むマップ。</span><span class="sxs-lookup"><span data-stu-id="84bce-166">A map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="84bce-167">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84bce-167">Each key contains a list of proxies.</span></span>

## <a name="method-getproxiescontainer"></a><span data-ttu-id="84bce-168">メソッド getProxiesContainer</span><span class="sxs-lookup"><span data-stu-id="84bce-168">Method getProxiesContainer</span></span>

<span data-ttu-id="84bce-169">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-169">Gets the proxies in this project.</span></span>

```xpp
public container getProxiesContainer()
```

### <a name="return-value---getproxiescontainer"></a><span data-ttu-id="84bce-170">戻り値 - getProxiesContainer</span><span class="sxs-lookup"><span data-stu-id="84bce-170">Return Value - getProxiesContainer</span></span>

<span data-ttu-id="84bce-171">マップの梱包済み表現を保持するコンテナーには、Class、Enum、Table のキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84bce-171">A container that holds the packed representation of a map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="84bce-172">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84bce-172">Each key contains a list of proxies.</span></span>

## <a name="method-getreferencedprojectsinaot"></a><span data-ttu-id="84bce-173">メソッド getReferencedProjectsInAOT</span><span class="sxs-lookup"><span data-stu-id="84bce-173">Method getReferencedProjectsInAOT</span></span>

<span data-ttu-id="84bce-174">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="84bce-174">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

```xpp
public str getReferencedProjectsInAOT()
```

### <a name="return-value---getreferencedprojectsinaot"></a><span data-ttu-id="84bce-175">戻り値 - getReferencedProjectsInAOT</span><span class="sxs-lookup"><span data-stu-id="84bce-175">Return Value - getReferencedProjectsInAOT</span></span>

<span data-ttu-id="84bce-176">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスの一覧。</span><span class="sxs-lookup"><span data-stu-id="84bce-176">A list of AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

## <a name="method-referencedprojects"></a><span data-ttu-id="84bce-177">メソッド referencedProjects</span><span class="sxs-lookup"><span data-stu-id="84bce-177">Method referencedProjects</span></span>

```xpp
public str referencedProjects([str value])
```

### <a name="parameters---referencedprojects"></a><span data-ttu-id="84bce-178">パラメーター - referencedProjects</span><span class="sxs-lookup"><span data-stu-id="84bce-178">Parameters - referencedProjects</span></span>

<span data-ttu-id="84bce-179">値</span><span class="sxs-lookup"><span data-stu-id="84bce-179">value</span></span>  

### <a name="return-value---referencedprojects"></a><span data-ttu-id="84bce-180">戻り値 - referencedProjects</span><span class="sxs-lookup"><span data-stu-id="84bce-180">Return Value - referencedProjects</span></span>

## <a name="method-setprimarytargetfilename"></a><span data-ttu-id="84bce-181">メソッド setPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="84bce-181">Method setPrimaryTargetFileName</span></span>

<span data-ttu-id="84bce-182">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="84bce-182">Sets the primary target file name of the Visual Studio project.</span></span>

```xpp
public void setPrimaryTargetFileName(str targetFileName)
```

### <a name="parameters---setprimarytargetfilename"></a><span data-ttu-id="84bce-183">パラメーター - setPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="84bce-183">Parameters - setPrimaryTargetFileName</span></span>

<span data-ttu-id="84bce-184">targetFileName</span><span class="sxs-lookup"><span data-stu-id="84bce-184">targetFileName</span></span>  
<span data-ttu-id="84bce-185">Visual Studio プロジェクトのプライマリ ターゲット ファイル名。</span><span class="sxs-lookup"><span data-stu-id="84bce-185">The primary target file name of the Visual Studio project.</span></span>

## <a name="method-extracttospecificdir"></a><span data-ttu-id="84bce-186">メソッド extractToSpecificDir</span><span class="sxs-lookup"><span data-stu-id="84bce-186">Method extractToSpecificDir</span></span>

```xpp
public void extractToSpecificDir(str directory)
```

### <a name="parameters---extracttospecificdir"></a><span data-ttu-id="84bce-187">パラメーター - extractToSpecificDir</span><span class="sxs-lookup"><span data-stu-id="84bce-187">Parameters - extractToSpecificDir</span></span>

<span data-ttu-id="84bce-188">directory</span><span class="sxs-lookup"><span data-stu-id="84bce-188">directory</span></span>  

## <a name="method-setdeployto"></a><span data-ttu-id="84bce-189">メソッド setDeployTo</span><span class="sxs-lookup"><span data-stu-id="84bce-189">Method setDeployTo</span></span>

<span data-ttu-id="84bce-190">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="84bce-190">Sets the value of the deployTo property.</span></span>

```xpp
public void setDeployTo(DeployTo deployTo)
```

### <a name="parameters---setdeployto"></a><span data-ttu-id="84bce-191">パラメーター - setDeployTo</span><span class="sxs-lookup"><span data-stu-id="84bce-191">Parameters - setDeployTo</span></span>

<span data-ttu-id="84bce-192">deployTo</span><span class="sxs-lookup"><span data-stu-id="84bce-192">deployTo</span></span>  
<span data-ttu-id="84bce-193">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="84bce-193">The deployTo property value.</span></span>

