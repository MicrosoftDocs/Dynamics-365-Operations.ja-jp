---
title: VSProjectLinkNode クラス
description: このトピックでは、VSProjectLinkNode クラスについて説明します。
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
ms.openlocfilehash: 0c98e2c992e0798005cc496f9164d09c4c7d00f6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502694"
---
# <a name="class-vsprojectlinknode"></a><span data-ttu-id="fcbce-103">クラス VSProjectLinkNode</span><span class="sxs-lookup"><span data-stu-id="fcbce-103">Class VSProjectLinkNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectLinkNode extends VSItemNode
```

<span data-ttu-id="fcbce-104">VSProjectLinkNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードにある別の AOT へのリンクを表します。</span><span class="sxs-lookup"><span data-stu-id="fcbce-104">The VSProjectLinkNode class represents links to other Application Object Tree (AOT) nodes in the Microsoft Visual Studio project nodes in the AOT.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbce-105">備考</span><span class="sxs-lookup"><span data-stu-id="fcbce-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fcbce-106">例</span><span class="sxs-lookup"><span data-stu-id="fcbce-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fcbce-107">方法</span><span class="sxs-lookup"><span data-stu-id="fcbce-107">Methods</span></span>

| <span data-ttu-id="fcbce-108">方法</span><span class="sxs-lookup"><span data-stu-id="fcbce-108">Method</span></span>                                                             | <span data-ttu-id="fcbce-109">説明</span><span class="sxs-lookup"><span data-stu-id="fcbce-109">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="fcbce-110">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="fcbce-110">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="fcbce-111">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="fcbce-111">Returns the source code of this node.</span></span> |
| <span data-ttu-id="fcbce-112">public str getAOTPath()</span><span class="sxs-lookup"><span data-stu-id="fcbce-112">public str getAOTPath()</span></span>                                            |                                       |
| <span data-ttu-id="fcbce-113">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="fcbce-113">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="fcbce-114">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="fcbce-114">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="fcbce-115">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="fcbce-115">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="fcbce-116">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="fcbce-116">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="fcbce-117">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="fcbce-117">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="fcbce-118">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="fcbce-118">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="fcbce-119">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="fcbce-119">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="fcbce-120">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcbce-120">Sets the source code of this node.</span></span>    |
| <span data-ttu-id="fcbce-121">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="fcbce-121">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="fcbce-122">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="fcbce-122">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |

## <a name="method-aotgetsource"></a><span data-ttu-id="fcbce-123">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-123">Method AOTgetSource</span></span>

<span data-ttu-id="fcbce-124">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="fcbce-124">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="fcbce-125">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-125">Return Value - AOTgetSource</span></span>

<span data-ttu-id="fcbce-126">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="fcbce-126">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="fcbce-127">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-127">Remarks - AOTgetSource</span></span>

<span data-ttu-id="fcbce-128">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="fcbce-128">This function is overridden by nodes that have source code.</span></span>

## <a name="method-getaotpath"></a><span data-ttu-id="fcbce-129">メソッド getAOTPath</span><span class="sxs-lookup"><span data-stu-id="fcbce-129">Method getAOTPath</span></span>

```xpp
public str getAOTPath()
```

### <a name="return-value---getaotpath"></a><span data-ttu-id="fcbce-130">戻り値 - getAOTPath</span><span class="sxs-lookup"><span data-stu-id="fcbce-130">Return Value - getAOTPath</span></span>

## <a name="method-getfiledata"></a><span data-ttu-id="fcbce-131">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="fcbce-131">Method getFileData</span></span>

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a><span data-ttu-id="fcbce-132">戻り値 - getFileData</span><span class="sxs-lookup"><span data-stu-id="fcbce-132">Return Value - getFileData</span></span>

## <a name="method-notifyfilecreated"></a><span data-ttu-id="fcbce-133">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="fcbce-133">Method notifyFileCreated</span></span>

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a><span data-ttu-id="fcbce-134">パラメーター - notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="fcbce-134">Parameters - notifyFileCreated</span></span>

<span data-ttu-id="fcbce-135">node</span><span class="sxs-lookup"><span data-stu-id="fcbce-135">node</span></span>  

## <a name="method-setfile"></a><span data-ttu-id="fcbce-136">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="fcbce-136">Method setFile</span></span>

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a><span data-ttu-id="fcbce-137">パラメーター - setFile</span><span class="sxs-lookup"><span data-stu-id="fcbce-137">Parameters - setFile</span></span>

<span data-ttu-id="fcbce-138">fileName</span><span class="sxs-lookup"><span data-stu-id="fcbce-138">fileName</span></span>  

## <a name="method-setfiledata"></a><span data-ttu-id="fcbce-139">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="fcbce-139">Method setFileData</span></span>

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a><span data-ttu-id="fcbce-140">パラメーター - setFileData</span><span class="sxs-lookup"><span data-stu-id="fcbce-140">Parameters - setFileData</span></span>

<span data-ttu-id="fcbce-141">データ</span><span class="sxs-lookup"><span data-stu-id="fcbce-141">data</span></span>  

## <a name="method-getfile"></a><span data-ttu-id="fcbce-142">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="fcbce-142">Method getFile</span></span>

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a><span data-ttu-id="fcbce-143">パラメーター - getFile</span><span class="sxs-lookup"><span data-stu-id="fcbce-143">Parameters - getFile</span></span>

<span data-ttu-id="fcbce-144">fileName</span><span class="sxs-lookup"><span data-stu-id="fcbce-144">fileName</span></span>  

## <a name="method-notifyfileupdated"></a><span data-ttu-id="fcbce-145">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="fcbce-145">Method notifyFileUpdated</span></span>

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a><span data-ttu-id="fcbce-146">パラメーター - notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="fcbce-146">Parameters - notifyFileUpdated</span></span>

<span data-ttu-id="fcbce-147">node</span><span class="sxs-lookup"><span data-stu-id="fcbce-147">node</span></span>  

## <a name="method-aotsetsource"></a><span data-ttu-id="fcbce-148">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-148">Method AOTsetSource</span></span>

<span data-ttu-id="fcbce-149">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcbce-149">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="fcbce-150">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-150">Parameters - AOTsetSource</span></span>

<span data-ttu-id="fcbce-151">ソース</span><span class="sxs-lookup"><span data-stu-id="fcbce-151">source</span></span>  
<span data-ttu-id="fcbce-152">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fcbce-152">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="fcbce-153">isStatic</span><span class="sxs-lookup"><span data-stu-id="fcbce-153">isStatic</span></span>  
<span data-ttu-id="fcbce-154">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fcbce-154">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="fcbce-155">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="fcbce-155">Remarks - AOTsetSource</span></span>

<span data-ttu-id="fcbce-156">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="fcbce-156">This method is overridden by nodes that have source code.</span></span>

## <a name="method-notifyfilerenamed"></a><span data-ttu-id="fcbce-157">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="fcbce-157">Method notifyFileRenamed</span></span>

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a><span data-ttu-id="fcbce-158">パラメーター - notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="fcbce-158">Parameters - notifyFileRenamed</span></span>

<span data-ttu-id="fcbce-159">node</span><span class="sxs-lookup"><span data-stu-id="fcbce-159">node</span></span>  

<!-- -->

<span data-ttu-id="fcbce-160">oldName</span><span class="sxs-lookup"><span data-stu-id="fcbce-160">oldName</span></span>  

## <a name="method-notifyfiledeleted"></a><span data-ttu-id="fcbce-161">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="fcbce-161">Method notifyFileDeleted</span></span>

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a><span data-ttu-id="fcbce-162">パラメーター - notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="fcbce-162">Parameters - notifyFileDeleted</span></span>

<span data-ttu-id="fcbce-163">node</span><span class="sxs-lookup"><span data-stu-id="fcbce-163">node</span></span>  

<!-- -->

<span data-ttu-id="fcbce-164">aotPath</span><span class="sxs-lookup"><span data-stu-id="fcbce-164">aotPath</span></span>  

