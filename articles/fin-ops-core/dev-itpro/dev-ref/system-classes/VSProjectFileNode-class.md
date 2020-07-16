---
title: VSProjectFileNode クラス
description: このトピックでは、VSProjectFileNode クラスについて説明します。
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
ms.openlocfilehash: 104080111549833c0706d6ef5b472e65a65f6b97
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502696"
---
# <a name="class-vsprojectfilenode"></a><span data-ttu-id="d1dfc-103">クラス VSProjectFileNode</span><span class="sxs-lookup"><span data-stu-id="d1dfc-103">Class VSProjectFileNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectFileNode extends VSItemNode
```

<span data-ttu-id="d1dfc-104">VSProjectFileNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-104">The VSProjectFileNode class represents files in the Microsoft Visual Studio project nodes in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1dfc-105">備考</span><span class="sxs-lookup"><span data-stu-id="d1dfc-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d1dfc-106">例</span><span class="sxs-lookup"><span data-stu-id="d1dfc-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d1dfc-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="d1dfc-107">Methods</span></span>

| <span data-ttu-id="d1dfc-108">方法</span><span class="sxs-lookup"><span data-stu-id="d1dfc-108">Method</span></span>                                                             | <span data-ttu-id="d1dfc-109">説明</span><span class="sxs-lookup"><span data-stu-id="d1dfc-109">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="d1dfc-110">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="d1dfc-110">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="d1dfc-111">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-111">Returns the source code of this node.</span></span> |
| <span data-ttu-id="d1dfc-112">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="d1dfc-112">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="d1dfc-113">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-113">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="d1dfc-114">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-114">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="d1dfc-115">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-115">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="d1dfc-116">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-116">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |
| <span data-ttu-id="d1dfc-117">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-117">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="d1dfc-118">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-118">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="d1dfc-119">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="d1dfc-119">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="d1dfc-120">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="d1dfc-120">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="d1dfc-121">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-121">Sets the source code of this node.</span></span>    |

## <a name="method-aotgetsource"></a><span data-ttu-id="d1dfc-122">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-122">Method AOTgetSource</span></span>

<span data-ttu-id="d1dfc-123">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-123">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="d1dfc-124">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-124">Return Value - AOTgetSource</span></span>

<span data-ttu-id="d1dfc-125">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-125">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="d1dfc-126">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-126">Remarks - AOTgetSource</span></span>

<span data-ttu-id="d1dfc-127">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-127">This function is overridden by nodes that have source code.</span></span>

## <a name="method-getfiledata"></a><span data-ttu-id="d1dfc-128">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="d1dfc-128">Method getFileData</span></span>

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a><span data-ttu-id="d1dfc-129">戻り値 - getFileData</span><span class="sxs-lookup"><span data-stu-id="d1dfc-129">Return Value - getFileData</span></span>

## <a name="method-notifyfilecreated"></a><span data-ttu-id="d1dfc-130">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="d1dfc-130">Method notifyFileCreated</span></span>

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a><span data-ttu-id="d1dfc-131">パラメーター - notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="d1dfc-131">Parameters - notifyFileCreated</span></span>

<span data-ttu-id="d1dfc-132">node</span><span class="sxs-lookup"><span data-stu-id="d1dfc-132">node</span></span>  

## <a name="method-setfiledata"></a><span data-ttu-id="d1dfc-133">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="d1dfc-133">Method setFileData</span></span>

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a><span data-ttu-id="d1dfc-134">パラメーター - setFileData</span><span class="sxs-lookup"><span data-stu-id="d1dfc-134">Parameters - setFileData</span></span>

<span data-ttu-id="d1dfc-135">データ</span><span class="sxs-lookup"><span data-stu-id="d1dfc-135">data</span></span>  

## <a name="method-getfile"></a><span data-ttu-id="d1dfc-136">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="d1dfc-136">Method getFile</span></span>

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a><span data-ttu-id="d1dfc-137">パラメーター - getFile</span><span class="sxs-lookup"><span data-stu-id="d1dfc-137">Parameters - getFile</span></span>

<span data-ttu-id="d1dfc-138">fileName</span><span class="sxs-lookup"><span data-stu-id="d1dfc-138">fileName</span></span>  

## <a name="method-notifyfiledeleted"></a><span data-ttu-id="d1dfc-139">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="d1dfc-139">Method notifyFileDeleted</span></span>

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a><span data-ttu-id="d1dfc-140">パラメーター - notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="d1dfc-140">Parameters - notifyFileDeleted</span></span>

<span data-ttu-id="d1dfc-141">node</span><span class="sxs-lookup"><span data-stu-id="d1dfc-141">node</span></span>  

<!-- -->

<span data-ttu-id="d1dfc-142">aotPath</span><span class="sxs-lookup"><span data-stu-id="d1dfc-142">aotPath</span></span>  

## <a name="method-notifyfileupdated"></a><span data-ttu-id="d1dfc-143">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="d1dfc-143">Method notifyFileUpdated</span></span>

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a><span data-ttu-id="d1dfc-144">パラメーター - notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="d1dfc-144">Parameters - notifyFileUpdated</span></span>

<span data-ttu-id="d1dfc-145">node</span><span class="sxs-lookup"><span data-stu-id="d1dfc-145">node</span></span>  

## <a name="method-setfile"></a><span data-ttu-id="d1dfc-146">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="d1dfc-146">Method setFile</span></span>

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a><span data-ttu-id="d1dfc-147">パラメーター - setFile</span><span class="sxs-lookup"><span data-stu-id="d1dfc-147">Parameters - setFile</span></span>

<span data-ttu-id="d1dfc-148">fileName</span><span class="sxs-lookup"><span data-stu-id="d1dfc-148">fileName</span></span>  

## <a name="method-notifyfilerenamed"></a><span data-ttu-id="d1dfc-149">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="d1dfc-149">Method notifyFileRenamed</span></span>

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a><span data-ttu-id="d1dfc-150">パラメーター - notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="d1dfc-150">Parameters - notifyFileRenamed</span></span>

<span data-ttu-id="d1dfc-151">node</span><span class="sxs-lookup"><span data-stu-id="d1dfc-151">node</span></span>  

<!-- -->

<span data-ttu-id="d1dfc-152">oldName</span><span class="sxs-lookup"><span data-stu-id="d1dfc-152">oldName</span></span>  

## <a name="method-aotsetsource"></a><span data-ttu-id="d1dfc-153">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-153">Method AOTsetSource</span></span>

<span data-ttu-id="d1dfc-154">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-154">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="d1dfc-155">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-155">Parameters - AOTsetSource</span></span>

<span data-ttu-id="d1dfc-156">ソース</span><span class="sxs-lookup"><span data-stu-id="d1dfc-156">source</span></span>  
<span data-ttu-id="d1dfc-157">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-157">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="d1dfc-158">isStatic</span><span class="sxs-lookup"><span data-stu-id="d1dfc-158">isStatic</span></span>  
<span data-ttu-id="d1dfc-159">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-159">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="d1dfc-160">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="d1dfc-160">Remarks - AOTsetSource</span></span>

<span data-ttu-id="d1dfc-161">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d1dfc-161">This method is overridden by nodes that have source code.</span></span>

