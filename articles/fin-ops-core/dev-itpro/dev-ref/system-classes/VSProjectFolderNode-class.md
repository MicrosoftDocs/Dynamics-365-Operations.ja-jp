---
title: VSProjectFolderNode クラス
description: このトピックでは、VSProjectFolderNode クラスについて説明します。
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
ms.openlocfilehash: 23a621d60678b6504f55e533e9fa20c42f9addd5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502695"
---
# <a name="class-vsprojectfoldernode"></a><span data-ttu-id="11432-103">クラス VSProjectFolderNode</span><span class="sxs-lookup"><span data-stu-id="11432-103">Class VSProjectFolderNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectFolderNode extends TreeNode
```

<span data-ttu-id="11432-104">VSProjectFolderNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="11432-104">The VSProjectFolderNode class represents folders in the Microsoft Visual Studio project nodes in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="11432-105">備考</span><span class="sxs-lookup"><span data-stu-id="11432-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="11432-106">例</span><span class="sxs-lookup"><span data-stu-id="11432-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="11432-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="11432-107">Methods</span></span>

| <span data-ttu-id="11432-108">方法</span><span class="sxs-lookup"><span data-stu-id="11432-108">Method</span></span>                                                                                       | <span data-ttu-id="11432-109">説明</span><span class="sxs-lookup"><span data-stu-id="11432-109">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11432-110">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="11432-110">public str AOTgetSource()</span></span>                                                                    | <span data-ttu-id="11432-111">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="11432-111">Returns the source code of this node.</span></span>                                                                    |
| <span data-ttu-id="11432-112">public VSProjectFileNode createFileNode(str name)</span><span class="sxs-lookup"><span data-stu-id="11432-112">public VSProjectFileNode createFileNode(str name)</span></span>                                            | <span data-ttu-id="11432-113">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-113">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="11432-114">public VSProjectFolderNode createFolderNode(str name)</span><span class="sxs-lookup"><span data-stu-id="11432-114">public VSProjectFolderNode createFolderNode(str name)</span></span>                                        | <span data-ttu-id="11432-115">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-115">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span> |
| <span data-ttu-id="11432-116">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span><span class="sxs-lookup"><span data-stu-id="11432-116">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span></span> | <span data-ttu-id="11432-117">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-117">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="11432-118">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="11432-118">public BinData getFileData()</span></span>                                                                 |                                                                                                          |
| <span data-ttu-id="11432-119">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="11432-119">::public static void notifyFileUpdated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="11432-120">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="11432-120">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span>                           |                                                                                                          |
| <span data-ttu-id="11432-121">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="11432-121">public void setFileData(BinData data)</span></span>                                                        |                                                                                                          |
| <span data-ttu-id="11432-122">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="11432-122">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>                                   | <span data-ttu-id="11432-123">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11432-123">Sets the source code of this node.</span></span>                                                                       |
| <span data-ttu-id="11432-124">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="11432-124">public void getFile(str fileName)</span></span>                                                            |                                                                                                          |
| <span data-ttu-id="11432-125">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="11432-125">::public static void notifyFileCreated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="11432-126">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="11432-126">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span>                           |                                                                                                          |
| <span data-ttu-id="11432-127">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="11432-127">public void setFile(str fileName)</span></span>                                                            |                                                                                                          |

## <a name="method-aotgetsource"></a><span data-ttu-id="11432-128">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="11432-128">Method AOTgetSource</span></span>

<span data-ttu-id="11432-129">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="11432-129">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="11432-130">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="11432-130">Return Value - AOTgetSource</span></span>

<span data-ttu-id="11432-131">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="11432-131">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="11432-132">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="11432-132">Remarks - AOTgetSource</span></span>

<span data-ttu-id="11432-133">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="11432-133">This function is overridden by nodes that have source code.</span></span>

## <a name="method-createfilenode"></a><span data-ttu-id="11432-134">メソッド createFileNode</span><span class="sxs-lookup"><span data-stu-id="11432-134">Method createFileNode</span></span>

<span data-ttu-id="11432-135">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-135">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>

```xpp
public VSProjectFileNode createFileNode(str name)
```

### <a name="parameters---createfilenode"></a><span data-ttu-id="11432-136">パラメータ - createFileNode</span><span class="sxs-lookup"><span data-stu-id="11432-136">Parameters - createFileNode</span></span>

<span data-ttu-id="11432-137">名前</span><span class="sxs-lookup"><span data-stu-id="11432-137">name</span></span>  
<span data-ttu-id="11432-138">ファイル ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="11432-138">The name of the file node.</span></span>

### <a name="return-value---createfilenode"></a><span data-ttu-id="11432-139">戻り値 - createFileNode</span><span class="sxs-lookup"><span data-stu-id="11432-139">Return Value - createFileNode</span></span>

<span data-ttu-id="11432-140">VSProjectFileNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="11432-140">The new instance of the VSProjectFileNode class.</span></span>

## <a name="method-createfoldernode"></a><span data-ttu-id="11432-141">メソッド createFolderNode</span><span class="sxs-lookup"><span data-stu-id="11432-141">Method createFolderNode</span></span>

<span data-ttu-id="11432-142">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-142">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span>

```xpp
public VSProjectFolderNode createFolderNode(str name)
```

### <a name="parameters---createfoldernode"></a><span data-ttu-id="11432-143">パラメーター - createFolderNode</span><span class="sxs-lookup"><span data-stu-id="11432-143">Parameters - createFolderNode</span></span>

<span data-ttu-id="11432-144">名前</span><span class="sxs-lookup"><span data-stu-id="11432-144">name</span></span>  
<span data-ttu-id="11432-145">フォルダー ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="11432-145">The name of the folder node.</span></span>

### <a name="return-value---createfoldernode"></a><span data-ttu-id="11432-146">戻り値 - createFolderNode</span><span class="sxs-lookup"><span data-stu-id="11432-146">Return Value - createFolderNode</span></span>

<span data-ttu-id="11432-147">VSProjectFolderNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="11432-147">The new instance of the VSProjectFolderNode class.</span></span>

## <a name="method-createlinknode"></a><span data-ttu-id="11432-148">メソッド createLinkNode</span><span class="sxs-lookup"><span data-stu-id="11432-148">Method createLinkNode</span></span>

<span data-ttu-id="11432-149">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="11432-149">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>

```xpp
public VSProjectLinkNode createLinkNode(str name, str aotPath, [boolean createLinkedNode])
```

### <a name="parameters---createlinknode"></a><span data-ttu-id="11432-150">パラメーター - createLinkNode</span><span class="sxs-lookup"><span data-stu-id="11432-150">Parameters - createLinkNode</span></span>

<span data-ttu-id="11432-151">名前</span><span class="sxs-lookup"><span data-stu-id="11432-151">name</span></span>  

<!-- -->

<span data-ttu-id="11432-152">aotPath</span><span class="sxs-lookup"><span data-stu-id="11432-152">aotPath</span></span>  

<!-- -->

<span data-ttu-id="11432-153">createLinkedNode</span><span class="sxs-lookup"><span data-stu-id="11432-153">createLinkedNode</span></span>  

### <a name="return-value---createlinknode"></a><span data-ttu-id="11432-154">戻り値 - createLinkNode</span><span class="sxs-lookup"><span data-stu-id="11432-154">Return Value - createLinkNode</span></span>

<span data-ttu-id="11432-155">VSProjectLinkNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="11432-155">The new instance of the VSProjectLinkNode class.</span></span>

## <a name="method-getfiledata"></a><span data-ttu-id="11432-156">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="11432-156">Method getFileData</span></span>

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a><span data-ttu-id="11432-157">戻り値 - getFileData</span><span class="sxs-lookup"><span data-stu-id="11432-157">Return Value - getFileData</span></span>

## <a name="method-notifyfileupdated"></a><span data-ttu-id="11432-158">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="11432-158">Method notifyFileUpdated</span></span>

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a><span data-ttu-id="11432-159">パラメーター - notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="11432-159">Parameters - notifyFileUpdated</span></span>

<span data-ttu-id="11432-160">node</span><span class="sxs-lookup"><span data-stu-id="11432-160">node</span></span>  

## <a name="method-notifyfiledeleted"></a><span data-ttu-id="11432-161">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="11432-161">Method notifyFileDeleted</span></span>

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a><span data-ttu-id="11432-162">パラメーター - notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="11432-162">Parameters - notifyFileDeleted</span></span>

<span data-ttu-id="11432-163">node</span><span class="sxs-lookup"><span data-stu-id="11432-163">node</span></span>  

<!-- -->

<span data-ttu-id="11432-164">aotPath</span><span class="sxs-lookup"><span data-stu-id="11432-164">aotPath</span></span>  

## <a name="method-setfiledata"></a><span data-ttu-id="11432-165">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="11432-165">Method setFileData</span></span>

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a><span data-ttu-id="11432-166">パラメーター - setFileData</span><span class="sxs-lookup"><span data-stu-id="11432-166">Parameters - setFileData</span></span>

<span data-ttu-id="11432-167">データ</span><span class="sxs-lookup"><span data-stu-id="11432-167">data</span></span>  

## <a name="method-aotsetsource"></a><span data-ttu-id="11432-168">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="11432-168">Method AOTsetSource</span></span>

<span data-ttu-id="11432-169">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="11432-169">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="11432-170">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="11432-170">Parameters - AOTsetSource</span></span>

<span data-ttu-id="11432-171">ソース</span><span class="sxs-lookup"><span data-stu-id="11432-171">source</span></span>  
<span data-ttu-id="11432-172">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11432-172">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="11432-173">isStatic</span><span class="sxs-lookup"><span data-stu-id="11432-173">isStatic</span></span>  
<span data-ttu-id="11432-174">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="11432-174">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="11432-175">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="11432-175">Remarks - AOTsetSource</span></span>

<span data-ttu-id="11432-176">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="11432-176">This method is overridden by nodes that have source code.</span></span>

## <a name="method-getfile"></a><span data-ttu-id="11432-177">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="11432-177">Method getFile</span></span>

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a><span data-ttu-id="11432-178">パラメーター - getFile</span><span class="sxs-lookup"><span data-stu-id="11432-178">Parameters - getFile</span></span>

<span data-ttu-id="11432-179">fileName</span><span class="sxs-lookup"><span data-stu-id="11432-179">fileName</span></span>  

## <a name="method-notifyfilecreated"></a><span data-ttu-id="11432-180">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="11432-180">Method notifyFileCreated</span></span>

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a><span data-ttu-id="11432-181">パラメーター - notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="11432-181">Parameters - notifyFileCreated</span></span>

<span data-ttu-id="11432-182">node</span><span class="sxs-lookup"><span data-stu-id="11432-182">node</span></span>  

## <a name="method-notifyfilerenamed"></a><span data-ttu-id="11432-183">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="11432-183">Method notifyFileRenamed</span></span>

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a><span data-ttu-id="11432-184">パラメーター - notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="11432-184">Parameters - notifyFileRenamed</span></span>

<span data-ttu-id="11432-185">node</span><span class="sxs-lookup"><span data-stu-id="11432-185">node</span></span>  

<!-- -->

<span data-ttu-id="11432-186">oldName</span><span class="sxs-lookup"><span data-stu-id="11432-186">oldName</span></span>  

## <a name="method-setfile"></a><span data-ttu-id="11432-187">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="11432-187">Method setFile</span></span>

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a><span data-ttu-id="11432-188">パラメーター - setFile</span><span class="sxs-lookup"><span data-stu-id="11432-188">Parameters - setFile</span></span>

<span data-ttu-id="11432-189">fileName</span><span class="sxs-lookup"><span data-stu-id="11432-189">fileName</span></span>  

