---
title: VSItemNode クラス
description: このトピックでは、VSItemNode クラスについて説明します。
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
ms.openlocfilehash: 2dc8bf1d7eea3add3dc9145a788014a4eadedd9b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502697"
---
# <a name="class-vsitemnode"></a><span data-ttu-id="228aa-103">クラス VSItemNode</span><span class="sxs-lookup"><span data-stu-id="228aa-103">Class VSItemNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSItemNode extends TreeNode
```

<span data-ttu-id="228aa-104">VSItemNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="228aa-104">The VSItemNode class is a base class for Microsoft Visual Studio project nodes in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="228aa-105">備考</span><span class="sxs-lookup"><span data-stu-id="228aa-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="228aa-106">例</span><span class="sxs-lookup"><span data-stu-id="228aa-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="228aa-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="228aa-107">Methods</span></span>

| <span data-ttu-id="228aa-108">方法</span><span class="sxs-lookup"><span data-stu-id="228aa-108">Method</span></span>                                                             | <span data-ttu-id="228aa-109">説明</span><span class="sxs-lookup"><span data-stu-id="228aa-109">Description</span></span>                                          |
|--------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="228aa-110">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="228aa-110">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="228aa-111">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="228aa-111">Returns the source code of this node.</span></span>                |
| <span data-ttu-id="228aa-112">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="228aa-112">public BinData getFileData()</span></span>                                       |                                                      |
| <span data-ttu-id="228aa-113">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="228aa-113">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> | <span data-ttu-id="228aa-114">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-114">Notifies listeners that a file has been deleted.</span></span>     |
| <span data-ttu-id="228aa-115">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="228aa-115">::public static void notifyFileUpdated(TreeNode node)</span></span>              | <span data-ttu-id="228aa-116">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-116">Notifies listeners that a file has been updated.</span></span>     |
| <span data-ttu-id="228aa-117">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="228aa-117">public void setFileData(BinData data)</span></span>                              |                                                      |
| <span data-ttu-id="228aa-118">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="228aa-118">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="228aa-119">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="228aa-119">Sets the source code of this node.</span></span>                   |
| <span data-ttu-id="228aa-120">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="228aa-120">public void getFile(str fileName)</span></span>                                  |                                                      |
| <span data-ttu-id="228aa-121">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="228aa-121">::public static void notifyFileCreated(TreeNode node)</span></span>              | <span data-ttu-id="228aa-122">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-122">Notifies listeners that a new file has been created.</span></span> |
| <span data-ttu-id="228aa-123">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="228aa-123">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> | <span data-ttu-id="228aa-124">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-124">Notifies listeners that a file has been renamed.</span></span>     |
| <span data-ttu-id="228aa-125">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="228aa-125">public void setFile(str fileName)</span></span>                                  |                                                      |

## <a name="method-aotgetsource"></a><span data-ttu-id="228aa-126">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-126">Method AOTgetSource</span></span>

<span data-ttu-id="228aa-127">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="228aa-127">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="228aa-128">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-128">Return Value - AOTgetSource</span></span>

<span data-ttu-id="228aa-129">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="228aa-129">The string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="228aa-130">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-130">Remarks - AOTgetSource</span></span>

<span data-ttu-id="228aa-131">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="228aa-131">This function is overridden by nodes that have source code.</span></span>

## <a name="method-getfiledata"></a><span data-ttu-id="228aa-132">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="228aa-132">Method getFileData</span></span>

```xpp
public BinData getFileData()
```

### <a name="return-value---getfiledata"></a><span data-ttu-id="228aa-133">戻り値 - getFileData</span><span class="sxs-lookup"><span data-stu-id="228aa-133">Return Value - getFileData</span></span>

## <a name="method-notifyfiledeleted"></a><span data-ttu-id="228aa-134">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="228aa-134">Method notifyFileDeleted</span></span>

<span data-ttu-id="228aa-135">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-135">Notifies listeners that a file has been deleted.</span></span>

```xpp
public static void notifyFileDeleted(TreeNode node, str aotPath)
```

### <a name="parameters---notifyfiledeleted"></a><span data-ttu-id="228aa-136">パラメーター - notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="228aa-136">Parameters - notifyFileDeleted</span></span>

<span data-ttu-id="228aa-137">node</span><span class="sxs-lookup"><span data-stu-id="228aa-137">node</span></span>  
<span data-ttu-id="228aa-138">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="228aa-138">The AOT path of the file.</span></span>

<!-- -->

<span data-ttu-id="228aa-139">aotPath</span><span class="sxs-lookup"><span data-stu-id="228aa-139">aotPath</span></span>  
<span data-ttu-id="228aa-140">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="228aa-140">The AOT path of the file.</span></span>

## <a name="method-notifyfileupdated"></a><span data-ttu-id="228aa-141">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="228aa-141">Method notifyFileUpdated</span></span>

<span data-ttu-id="228aa-142">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-142">Notifies listeners that a file has been updated.</span></span>

```xpp
public static void notifyFileUpdated(TreeNode node)
```

### <a name="parameters---notifyfileupdated"></a><span data-ttu-id="228aa-143">パラメーター - notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="228aa-143">Parameters - notifyFileUpdated</span></span>

<span data-ttu-id="228aa-144">node</span><span class="sxs-lookup"><span data-stu-id="228aa-144">node</span></span>  
<span data-ttu-id="228aa-145">更新ノード。</span><span class="sxs-lookup"><span data-stu-id="228aa-145">The node that has been updated.</span></span>

## <a name="method-setfiledata"></a><span data-ttu-id="228aa-146">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="228aa-146">Method setFileData</span></span>

```xpp
public void setFileData(BinData data)
```

### <a name="parameters---setfiledata"></a><span data-ttu-id="228aa-147">パラメーター - setFileData</span><span class="sxs-lookup"><span data-stu-id="228aa-147">Parameters - setFileData</span></span>

<span data-ttu-id="228aa-148">データ</span><span class="sxs-lookup"><span data-stu-id="228aa-148">data</span></span>  

## <a name="method-aotsetsource"></a><span data-ttu-id="228aa-149">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-149">Method AOTsetSource</span></span>

<span data-ttu-id="228aa-150">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="228aa-150">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="228aa-151">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-151">Parameters - AOTsetSource</span></span>

<span data-ttu-id="228aa-152">ソース</span><span class="sxs-lookup"><span data-stu-id="228aa-152">source</span></span>  
<span data-ttu-id="228aa-153">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="228aa-153">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="228aa-154">isStatic</span><span class="sxs-lookup"><span data-stu-id="228aa-154">isStatic</span></span>  
<span data-ttu-id="228aa-155">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="228aa-155">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="228aa-156">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="228aa-156">Remarks - AOTsetSource</span></span>

<span data-ttu-id="228aa-157">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="228aa-157">This method is overridden by nodes that have source code.</span></span>

## <a name="method-getfile"></a><span data-ttu-id="228aa-158">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="228aa-158">Method getFile</span></span>

```xpp
public void getFile(str fileName)
```

### <a name="parameters---getfile"></a><span data-ttu-id="228aa-159">パラメーター - getFile</span><span class="sxs-lookup"><span data-stu-id="228aa-159">Parameters - getFile</span></span>

<span data-ttu-id="228aa-160">fileName</span><span class="sxs-lookup"><span data-stu-id="228aa-160">fileName</span></span>  

## <a name="method-notifyfilecreated"></a><span data-ttu-id="228aa-161">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="228aa-161">Method notifyFileCreated</span></span>

<span data-ttu-id="228aa-162">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-162">Notifies listeners that a new file has been created.</span></span>

```xpp
public static void notifyFileCreated(TreeNode node)
```

### <a name="parameters---notifyfilecreated"></a><span data-ttu-id="228aa-163">パラメーター - notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="228aa-163">Parameters - notifyFileCreated</span></span>

<span data-ttu-id="228aa-164">node</span><span class="sxs-lookup"><span data-stu-id="228aa-164">node</span></span>  
<span data-ttu-id="228aa-165">作成されたノード。</span><span class="sxs-lookup"><span data-stu-id="228aa-165">The node that has been created.</span></span>

## <a name="method-notifyfilerenamed"></a><span data-ttu-id="228aa-166">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="228aa-166">Method notifyFileRenamed</span></span>

<span data-ttu-id="228aa-167">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="228aa-167">Notifies listeners that a file has been renamed.</span></span>

```xpp
public static void notifyFileRenamed(TreeNode node, str oldName)
```

### <a name="parameters---notifyfilerenamed"></a><span data-ttu-id="228aa-168">パラメーター - notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="228aa-168">Parameters - notifyFileRenamed</span></span>

<span data-ttu-id="228aa-169">node</span><span class="sxs-lookup"><span data-stu-id="228aa-169">node</span></span>  
<span data-ttu-id="228aa-170">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="228aa-170">The old name of the file.</span></span>

<!-- -->

<span data-ttu-id="228aa-171">oldName</span><span class="sxs-lookup"><span data-stu-id="228aa-171">oldName</span></span>  
<span data-ttu-id="228aa-172">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="228aa-172">The old name of the file.</span></span>

## <a name="method-setfile"></a><span data-ttu-id="228aa-173">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="228aa-173">Method setFile</span></span>

```xpp
public void setFile(str fileName)
```

### <a name="parameters---setfile"></a><span data-ttu-id="228aa-174">パラメーター - setFile</span><span class="sxs-lookup"><span data-stu-id="228aa-174">Parameters - setFile</span></span>

<span data-ttu-id="228aa-175">fileName</span><span class="sxs-lookup"><span data-stu-id="228aa-175">fileName</span></span>  

