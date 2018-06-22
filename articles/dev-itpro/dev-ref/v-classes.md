---
title: "V クラス"
description: "文字 V で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55841
ms.assetid: fd3859a7-c0e5-41b3-9bd3-fc68099e727f
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69928f5519b2db5ece6df8f0ae9809211f2e10d8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="v-classes"></a><span data-ttu-id="68050-103">V クラス</span><span class="sxs-lookup"><span data-stu-id="68050-103">V Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68050-104">文字 V で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="68050-104">System API classes that start with the letter V.</span></span>

<a name="class-validateeventargs"></a><span data-ttu-id="68050-105">クラス ValidateEventArgs</span><span class="sxs-lookup"><span data-stu-id="68050-105">Class ValidateEventArgs</span></span>
-----------------------

    class ValidateEventArgs extends DataEventArgs

### <a name="remarks"></a><span data-ttu-id="68050-106">備考</span><span class="sxs-lookup"><span data-stu-id="68050-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-107">例</span><span class="sxs-lookup"><span data-stu-id="68050-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-108">Methods</span></span>

| <span data-ttu-id="68050-109">方法</span><span class="sxs-lookup"><span data-stu-id="68050-109">Method</span></span>                                                | <span data-ttu-id="68050-110">説明</span><span class="sxs-lookup"><span data-stu-id="68050-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| <span data-ttu-id="68050-111">public boolean parmValidateResult(\[boolean result\])</span><span class="sxs-lookup"><span data-stu-id="68050-111">public boolean parmValidateResult(\[boolean result\])</span></span> |             |
| <span data-ttu-id="68050-112">public void new(boolean result)</span><span class="sxs-lookup"><span data-stu-id="68050-112">public void new(boolean result)</span></span>                       |             |

### <a name="method-parmvalidateresult"></a><span data-ttu-id="68050-113">メソッド parmValidateResult</span><span class="sxs-lookup"><span data-stu-id="68050-113">Method parmValidateResult</span></span>

    public boolean parmValidateResult([boolean result])

#### <a name="parameters"></a><span data-ttu-id="68050-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-114">Parameters</span></span>

<span data-ttu-id="68050-115">件の結果</span><span class="sxs-lookup"><span data-stu-id="68050-115">result</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-116">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="68050-117">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-117">Method new</span></span>

    public void new(boolean result)

#### <a name="parameters"></a><span data-ttu-id="68050-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-118">Parameters</span></span>

<span data-ttu-id="68050-119">件の結果</span><span class="sxs-lookup"><span data-stu-id="68050-119">result</span></span>  

## <a name="class-validatefieldeventargs"></a><span data-ttu-id="68050-120">クラス ValidateFieldEventArgs</span><span class="sxs-lookup"><span data-stu-id="68050-120">Class ValidateFieldEventArgs</span></span>
    class ValidateFieldEventArgs extends ValidateEventArgs

### <a name="remarks"></a><span data-ttu-id="68050-121">備考</span><span class="sxs-lookup"><span data-stu-id="68050-121">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-122">例</span><span class="sxs-lookup"><span data-stu-id="68050-122">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-123">Methods</span></span>

| <span data-ttu-id="68050-124">方法</span><span class="sxs-lookup"><span data-stu-id="68050-124">Method</span></span>                                       | <span data-ttu-id="68050-125">説明</span><span class="sxs-lookup"><span data-stu-id="68050-125">Description</span></span> |
|----------------------------------------------|-------------|
| <span data-ttu-id="68050-126">public int parmFieldId()</span><span class="sxs-lookup"><span data-stu-id="68050-126">public int parmFieldId()</span></span>                     |             |
| <span data-ttu-id="68050-127">public void new(int fieldId, boolean result)</span><span class="sxs-lookup"><span data-stu-id="68050-127">public void new(int fieldId, boolean result)</span></span> |             |

### <a name="method-parmfieldid"></a><span data-ttu-id="68050-128">メソッド parmFieldId</span><span class="sxs-lookup"><span data-stu-id="68050-128">Method parmFieldId</span></span>

    public int parmFieldId()

#### <a name="return-value"></a><span data-ttu-id="68050-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-129">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="68050-130">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-130">Method new</span></span>

    public void new(int fieldId, boolean result)

#### <a name="parameters"></a><span data-ttu-id="68050-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-131">Parameters</span></span>

<span data-ttu-id="68050-132">fieldId</span><span class="sxs-lookup"><span data-stu-id="68050-132">fieldId</span></span>  

<!-- -->

<span data-ttu-id="68050-133">件の結果</span><span class="sxs-lookup"><span data-stu-id="68050-133">result</span></span>  

## <a name="class-validatefieldvalueeventargs"></a><span data-ttu-id="68050-134">クラス ValidateFieldValueEventArgs</span><span class="sxs-lookup"><span data-stu-id="68050-134">Class ValidateFieldValueEventArgs</span></span>
    class ValidateFieldValueEventArgs extends ValidateEventArgs

### <a name="remarks"></a><span data-ttu-id="68050-135">備考</span><span class="sxs-lookup"><span data-stu-id="68050-135">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-136">例</span><span class="sxs-lookup"><span data-stu-id="68050-136">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-137">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-137">Methods</span></span>

| <span data-ttu-id="68050-138">方法</span><span class="sxs-lookup"><span data-stu-id="68050-138">Method</span></span>                                                         | <span data-ttu-id="68050-139">説明</span><span class="sxs-lookup"><span data-stu-id="68050-139">Description</span></span> |
|----------------------------------------------------------------|-------------|
| <span data-ttu-id="68050-140">public str parmFieldName()</span><span class="sxs-lookup"><span data-stu-id="68050-140">public str parmFieldName()</span></span>                                     |             |
| <span data-ttu-id="68050-141">public int parmArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="68050-141">public int parmArrayIndex()</span></span>                                    |             |
| <span data-ttu-id="68050-142">public void new(str fieldName, int arrayIndex, boolean result)</span><span class="sxs-lookup"><span data-stu-id="68050-142">public void new(str fieldName, int arrayIndex, boolean result)</span></span> |             |

### <a name="method-parmfieldname"></a><span data-ttu-id="68050-143">メソッド parmFieldName</span><span class="sxs-lookup"><span data-stu-id="68050-143">Method parmFieldName</span></span>

    public str parmFieldName()

#### <a name="return-value"></a><span data-ttu-id="68050-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-144">Return Value</span></span>

### <a name="method-parmarrayindex"></a><span data-ttu-id="68050-145">メソッド parmArrayIndex</span><span class="sxs-lookup"><span data-stu-id="68050-145">Method parmArrayIndex</span></span>

    public int parmArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="68050-146">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-146">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="68050-147">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-147">Method new</span></span>

    public void new(str fieldName, int arrayIndex, boolean result)

#### <a name="parameters"></a><span data-ttu-id="68050-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-148">Parameters</span></span>

<span data-ttu-id="68050-149">fieldName</span><span class="sxs-lookup"><span data-stu-id="68050-149">fieldName</span></span>  

<!-- -->

<span data-ttu-id="68050-150">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="68050-150">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="68050-151">件の結果</span><span class="sxs-lookup"><span data-stu-id="68050-151">result</span></span>  

## <a name="class-virtualchannelmanager"></a><span data-ttu-id="68050-152">クラス VirtualChannelManager</span><span class="sxs-lookup"><span data-stu-id="68050-152">Class VirtualChannelManager</span></span>
    class VirtualChannelManager extends Object

### <a name="remarks"></a><span data-ttu-id="68050-153">備考</span><span class="sxs-lookup"><span data-stu-id="68050-153">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-154">例</span><span class="sxs-lookup"><span data-stu-id="68050-154">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-155">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-155">Methods</span></span>

| <span data-ttu-id="68050-156">方法</span><span class="sxs-lookup"><span data-stu-id="68050-156">Method</span></span>                                         | <span data-ttu-id="68050-157">説明</span><span class="sxs-lookup"><span data-stu-id="68050-157">Description</span></span>                                                    |
|------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="68050-158">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="68050-158">public void finalize()</span></span>                         |                                                                |
| <span data-ttu-id="68050-159">public void new()</span><span class="sxs-lookup"><span data-stu-id="68050-159">public void new()</span></span>                              | <span data-ttu-id="68050-160">VirtualChannelManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-160">Initializes a new instance of the VirtualChannelManager class.</span></span> |
| <span data-ttu-id="68050-161">public void sendData(int listenerId, str data)</span><span class="sxs-lookup"><span data-stu-id="68050-161">public void sendData(int listenerId, str data)</span></span> |                                                                |

### <a name="method-finalize"></a><span data-ttu-id="68050-162">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="68050-162">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="68050-163">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-163">Method new</span></span>

<span data-ttu-id="68050-164">VirtualChannelManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-164">Initializes a new instance of the VirtualChannelManager class.</span></span>

    public void new()

### <a name="method-senddata"></a><span data-ttu-id="68050-165">メソッド sendData</span><span class="sxs-lookup"><span data-stu-id="68050-165">Method sendData</span></span>

    public void sendData(int listenerId, str data)

#### <a name="parameters"></a><span data-ttu-id="68050-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-166">Parameters</span></span>

<span data-ttu-id="68050-167">listenerId</span><span class="sxs-lookup"><span data-stu-id="68050-167">listenerId</span></span>  

<!-- -->

<span data-ttu-id="68050-168">データ</span><span class="sxs-lookup"><span data-stu-id="68050-168">data</span></span>  

## <a name="class-vsitemnode"></a><span data-ttu-id="68050-169">クラス VSItemNode</span><span class="sxs-lookup"><span data-stu-id="68050-169">Class VSItemNode</span></span>
    class VSItemNode extends TreeNode

<span data-ttu-id="68050-170">VSItemNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="68050-170">The VSItemNode class is a base class for Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-171">備考</span><span class="sxs-lookup"><span data-stu-id="68050-171">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-172">例</span><span class="sxs-lookup"><span data-stu-id="68050-172">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-173">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-173">Methods</span></span>

| <span data-ttu-id="68050-174">方法</span><span class="sxs-lookup"><span data-stu-id="68050-174">Method</span></span>                                                             | <span data-ttu-id="68050-175">説明</span><span class="sxs-lookup"><span data-stu-id="68050-175">Description</span></span>                                          |
|--------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68050-176">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="68050-176">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="68050-177">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-177">Returns the source code of this node.</span></span>                |
| <span data-ttu-id="68050-178">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="68050-178">public BinData getFileData()</span></span>                                       |                                                      |
| <span data-ttu-id="68050-179">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="68050-179">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> | <span data-ttu-id="68050-180">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-180">Notifies listeners that a file has been deleted.</span></span>     |
| <span data-ttu-id="68050-181">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-181">::public static void notifyFileUpdated(TreeNode node)</span></span>              | <span data-ttu-id="68050-182">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-182">Notifies listeners that a file has been updated.</span></span>     |
| <span data-ttu-id="68050-183">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="68050-183">public void setFileData(BinData data)</span></span>                              |                                                      |
| <span data-ttu-id="68050-184">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="68050-184">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="68050-185">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-185">Sets the source code of this node.</span></span>                   |
| <span data-ttu-id="68050-186">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-186">public void getFile(str fileName)</span></span>                                  |                                                      |
| <span data-ttu-id="68050-187">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-187">::public static void notifyFileCreated(TreeNode node)</span></span>              | <span data-ttu-id="68050-188">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-188">Notifies listeners that a new file has been created.</span></span> |
| <span data-ttu-id="68050-189">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="68050-189">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> | <span data-ttu-id="68050-190">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-190">Notifies listeners that a file has been renamed.</span></span>     |
| <span data-ttu-id="68050-191">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-191">public void setFile(str fileName)</span></span>                                  |                                                      |

### <a name="method-aotgetsource"></a><span data-ttu-id="68050-192">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="68050-192">Method AOTgetSource</span></span>

<span data-ttu-id="68050-193">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-193">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="68050-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-194">Return Value</span></span>

<span data-ttu-id="68050-195">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="68050-195">The string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-196">備考</span><span class="sxs-lookup"><span data-stu-id="68050-196">Remarks</span></span>

<span data-ttu-id="68050-197">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="68050-197">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="68050-198">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="68050-198">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="68050-199">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-199">Return Value</span></span>

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="68050-200">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="68050-200">Method notifyFileDeleted</span></span>

<span data-ttu-id="68050-201">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-201">Notifies listeners that a file has been deleted.</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="68050-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-202">Parameters</span></span>

<span data-ttu-id="68050-203">node</span><span class="sxs-lookup"><span data-stu-id="68050-203">node</span></span>  
<span data-ttu-id="68050-204">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="68050-204">The AOT path of the file.</span></span>

<!-- -->

<span data-ttu-id="68050-205">aotPath</span><span class="sxs-lookup"><span data-stu-id="68050-205">aotPath</span></span>  
<span data-ttu-id="68050-206">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="68050-206">The AOT path of the file.</span></span>

### <a name="method-notifyfileupdated"></a><span data-ttu-id="68050-207">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="68050-207">Method notifyFileUpdated</span></span>

<span data-ttu-id="68050-208">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-208">Notifies listeners that a file has been updated.</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-209">Parameters</span></span>

<span data-ttu-id="68050-210">node</span><span class="sxs-lookup"><span data-stu-id="68050-210">node</span></span>  
<span data-ttu-id="68050-211">更新ノード。</span><span class="sxs-lookup"><span data-stu-id="68050-211">The node that has been updated.</span></span>

### <a name="method-setfiledata"></a><span data-ttu-id="68050-212">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="68050-212">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="68050-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-213">Parameters</span></span>

<span data-ttu-id="68050-214">データ</span><span class="sxs-lookup"><span data-stu-id="68050-214">data</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="68050-215">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="68050-215">Method AOTsetSource</span></span>

<span data-ttu-id="68050-216">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-216">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="68050-217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-217">Parameters</span></span>

<span data-ttu-id="68050-218">ソース</span><span class="sxs-lookup"><span data-stu-id="68050-218">source</span></span>  
<span data-ttu-id="68050-219">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-219">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="68050-220">isStatic</span><span class="sxs-lookup"><span data-stu-id="68050-220">isStatic</span></span>  
<span data-ttu-id="68050-221">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-221">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-222">備考</span><span class="sxs-lookup"><span data-stu-id="68050-222">Remarks</span></span>

<span data-ttu-id="68050-223">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="68050-223">This method is overridden by nodes that have source code.</span></span>

### <a name="method-getfile"></a><span data-ttu-id="68050-224">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="68050-224">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-225">Parameters</span></span>

<span data-ttu-id="68050-226">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-226">fileName</span></span>  

### <a name="method-notifyfilecreated"></a><span data-ttu-id="68050-227">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="68050-227">Method notifyFileCreated</span></span>

<span data-ttu-id="68050-228">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-228">Notifies listeners that a new file has been created.</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-229">Parameters</span></span>

<span data-ttu-id="68050-230">node</span><span class="sxs-lookup"><span data-stu-id="68050-230">node</span></span>  
<span data-ttu-id="68050-231">作成されたノード。</span><span class="sxs-lookup"><span data-stu-id="68050-231">The node that has been created.</span></span>

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="68050-232">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="68050-232">Method notifyFileRenamed</span></span>

<span data-ttu-id="68050-233">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="68050-233">Notifies listeners that a file has been renamed.</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="68050-234">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-234">Parameters</span></span>

<span data-ttu-id="68050-235">node</span><span class="sxs-lookup"><span data-stu-id="68050-235">node</span></span>  
<span data-ttu-id="68050-236">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="68050-236">The old name of the file.</span></span>

<!-- -->

<span data-ttu-id="68050-237">oldName</span><span class="sxs-lookup"><span data-stu-id="68050-237">oldName</span></span>  
<span data-ttu-id="68050-238">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="68050-238">The old name of the file.</span></span>

### <a name="method-setfile"></a><span data-ttu-id="68050-239">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="68050-239">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-240">Parameters</span></span>

<span data-ttu-id="68050-241">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-241">fileName</span></span>  

## <a name="class-vsprojectfilenode"></a><span data-ttu-id="68050-242">クラス VSProjectFileNode</span><span class="sxs-lookup"><span data-stu-id="68050-242">Class VSProjectFileNode</span></span>
    class VSProjectFileNode extends VSItemNode

<span data-ttu-id="68050-243">VSProjectFileNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="68050-243">The VSProjectFileNode class represents files in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-244">備考</span><span class="sxs-lookup"><span data-stu-id="68050-244">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-245">例</span><span class="sxs-lookup"><span data-stu-id="68050-245">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-246">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-246">Methods</span></span>

| <span data-ttu-id="68050-247">方法</span><span class="sxs-lookup"><span data-stu-id="68050-247">Method</span></span>                                                             | <span data-ttu-id="68050-248">説明</span><span class="sxs-lookup"><span data-stu-id="68050-248">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="68050-249">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="68050-249">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="68050-250">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-250">Returns the source code of this node.</span></span> |
| <span data-ttu-id="68050-251">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="68050-251">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="68050-252">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-252">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="68050-253">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="68050-253">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="68050-254">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-254">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="68050-255">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="68050-255">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |
| <span data-ttu-id="68050-256">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-256">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="68050-257">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-257">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="68050-258">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="68050-258">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="68050-259">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="68050-259">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="68050-260">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-260">Sets the source code of this node.</span></span>    |

### <a name="method-aotgetsource"></a><span data-ttu-id="68050-261">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="68050-261">Method AOTgetSource</span></span>

<span data-ttu-id="68050-262">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-262">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="68050-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-263">Return Value</span></span>

<span data-ttu-id="68050-264">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="68050-264">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-265">備考</span><span class="sxs-lookup"><span data-stu-id="68050-265">Remarks</span></span>

<span data-ttu-id="68050-266">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="68050-266">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="68050-267">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="68050-267">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="68050-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-268">Return Value</span></span>

### <a name="method-notifyfilecreated"></a><span data-ttu-id="68050-269">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="68050-269">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-270">Parameters</span></span>

<span data-ttu-id="68050-271">node</span><span class="sxs-lookup"><span data-stu-id="68050-271">node</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="68050-272">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="68050-272">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="68050-273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-273">Parameters</span></span>

<span data-ttu-id="68050-274">データ</span><span class="sxs-lookup"><span data-stu-id="68050-274">data</span></span>  

### <a name="method-getfile"></a><span data-ttu-id="68050-275">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="68050-275">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-276">Parameters</span></span>

<span data-ttu-id="68050-277">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-277">fileName</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="68050-278">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="68050-278">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="68050-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-279">Parameters</span></span>

<span data-ttu-id="68050-280">node</span><span class="sxs-lookup"><span data-stu-id="68050-280">node</span></span>  

<!-- -->

<span data-ttu-id="68050-281">aotPath</span><span class="sxs-lookup"><span data-stu-id="68050-281">aotPath</span></span>  

### <a name="method-notifyfileupdated"></a><span data-ttu-id="68050-282">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="68050-282">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-283">Parameters</span></span>

<span data-ttu-id="68050-284">node</span><span class="sxs-lookup"><span data-stu-id="68050-284">node</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="68050-285">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="68050-285">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-286">Parameters</span></span>

<span data-ttu-id="68050-287">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-287">fileName</span></span>  

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="68050-288">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="68050-288">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="68050-289">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-289">Parameters</span></span>

<span data-ttu-id="68050-290">node</span><span class="sxs-lookup"><span data-stu-id="68050-290">node</span></span>  

<!-- -->

<span data-ttu-id="68050-291">oldName</span><span class="sxs-lookup"><span data-stu-id="68050-291">oldName</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="68050-292">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="68050-292">Method AOTsetSource</span></span>

<span data-ttu-id="68050-293">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-293">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="68050-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-294">Parameters</span></span>

<span data-ttu-id="68050-295">ソース</span><span class="sxs-lookup"><span data-stu-id="68050-295">source</span></span>  
<span data-ttu-id="68050-296">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-296">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="68050-297">isStatic</span><span class="sxs-lookup"><span data-stu-id="68050-297">isStatic</span></span>  
<span data-ttu-id="68050-298">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-298">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-299">備考</span><span class="sxs-lookup"><span data-stu-id="68050-299">Remarks</span></span>

<span data-ttu-id="68050-300">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="68050-300">This method is overridden by nodes that have source code.</span></span>

## <a name="class-vsprojectfoldernode"></a><span data-ttu-id="68050-301">クラス VSProjectFolderNode</span><span class="sxs-lookup"><span data-stu-id="68050-301">Class VSProjectFolderNode</span></span>
    class VSProjectFolderNode extends TreeNode

<span data-ttu-id="68050-302">VSProjectFolderNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="68050-302">The VSProjectFolderNode class represents folders in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-303">備考</span><span class="sxs-lookup"><span data-stu-id="68050-303">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-304">例</span><span class="sxs-lookup"><span data-stu-id="68050-304">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-305">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-305">Methods</span></span>

| <span data-ttu-id="68050-306">方法</span><span class="sxs-lookup"><span data-stu-id="68050-306">Method</span></span>                                                                                       | <span data-ttu-id="68050-307">説明</span><span class="sxs-lookup"><span data-stu-id="68050-307">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68050-308">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="68050-308">public str AOTgetSource()</span></span>                                                                    | <span data-ttu-id="68050-309">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-309">Returns the source code of this node.</span></span>                                                                    |
| <span data-ttu-id="68050-310">public VSProjectFileNode createFileNode(str name)</span><span class="sxs-lookup"><span data-stu-id="68050-310">public VSProjectFileNode createFileNode(str name)</span></span>                                            | <span data-ttu-id="68050-311">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-311">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="68050-312">public VSProjectFolderNode createFolderNode(str name)</span><span class="sxs-lookup"><span data-stu-id="68050-312">public VSProjectFolderNode createFolderNode(str name)</span></span>                                        | <span data-ttu-id="68050-313">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-313">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span> |
| <span data-ttu-id="68050-314">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span><span class="sxs-lookup"><span data-stu-id="68050-314">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span></span> | <span data-ttu-id="68050-315">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-315">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="68050-316">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="68050-316">public BinData getFileData()</span></span>                                                                 |                                                                                                          |
| <span data-ttu-id="68050-317">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-317">::public static void notifyFileUpdated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="68050-318">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="68050-318">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span>                           |                                                                                                          |
| <span data-ttu-id="68050-319">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="68050-319">public void setFileData(BinData data)</span></span>                                                        |                                                                                                          |
| <span data-ttu-id="68050-320">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="68050-320">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>                                   | <span data-ttu-id="68050-321">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-321">Sets the source code of this node.</span></span>                                                                       |
| <span data-ttu-id="68050-322">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-322">public void getFile(str fileName)</span></span>                                                            |                                                                                                          |
| <span data-ttu-id="68050-323">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-323">::public static void notifyFileCreated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="68050-324">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="68050-324">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span>                           |                                                                                                          |
| <span data-ttu-id="68050-325">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-325">public void setFile(str fileName)</span></span>                                                            |                                                                                                          |

### <a name="method-aotgetsource"></a><span data-ttu-id="68050-326">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="68050-326">Method AOTgetSource</span></span>

<span data-ttu-id="68050-327">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-327">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="68050-328">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-328">Return Value</span></span>

<span data-ttu-id="68050-329">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="68050-329">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-330">備考</span><span class="sxs-lookup"><span data-stu-id="68050-330">Remarks</span></span>

<span data-ttu-id="68050-331">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="68050-331">This function is overridden by nodes that have source code.</span></span>

### <a name="method-createfilenode"></a><span data-ttu-id="68050-332">メソッド createFileNode</span><span class="sxs-lookup"><span data-stu-id="68050-332">Method createFileNode</span></span>

<span data-ttu-id="68050-333">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-333">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectFileNode createFileNode(str name)

#### <a name="parameters"></a><span data-ttu-id="68050-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-334">Parameters</span></span>

<span data-ttu-id="68050-335">名前</span><span class="sxs-lookup"><span data-stu-id="68050-335">name</span></span>  
<span data-ttu-id="68050-336">ファイル ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="68050-336">The name of the file node.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-337">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-337">Return Value</span></span>

<span data-ttu-id="68050-338">VSProjectFileNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="68050-338">The new instance of the VSProjectFileNode class.</span></span>

### <a name="method-createfoldernode"></a><span data-ttu-id="68050-339">メソッド createFolderNode</span><span class="sxs-lookup"><span data-stu-id="68050-339">Method createFolderNode</span></span>

<span data-ttu-id="68050-340">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-340">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectFolderNode createFolderNode(str name)

#### <a name="parameters"></a><span data-ttu-id="68050-341">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-341">Parameters</span></span>

<span data-ttu-id="68050-342">名前</span><span class="sxs-lookup"><span data-stu-id="68050-342">name</span></span>  
<span data-ttu-id="68050-343">フォルダー ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="68050-343">The name of the folder node.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-344">Return Value</span></span>

<span data-ttu-id="68050-345">VSProjectFolderNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="68050-345">The new instance of the VSProjectFolderNode class.</span></span>

### <a name="method-createlinknode"></a><span data-ttu-id="68050-346">メソッド createLinkNode</span><span class="sxs-lookup"><span data-stu-id="68050-346">Method createLinkNode</span></span>

<span data-ttu-id="68050-347">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-347">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectLinkNode createLinkNode(str name, str aotPath, [boolean createLinkedNode])

#### <a name="parameters"></a><span data-ttu-id="68050-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-348">Parameters</span></span>

<span data-ttu-id="68050-349">名前</span><span class="sxs-lookup"><span data-stu-id="68050-349">name</span></span>  

<!-- -->

<span data-ttu-id="68050-350">aotPath</span><span class="sxs-lookup"><span data-stu-id="68050-350">aotPath</span></span>  

<!-- -->

<span data-ttu-id="68050-351">createLinkedNode</span><span class="sxs-lookup"><span data-stu-id="68050-351">createLinkedNode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-352">Return Value</span></span>

<span data-ttu-id="68050-353">VSProjectLinkNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="68050-353">The new instance of the VSProjectLinkNode class.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="68050-354">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="68050-354">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="68050-355">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-355">Return Value</span></span>

### <a name="method-notifyfileupdated"></a><span data-ttu-id="68050-356">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="68050-356">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-357">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-357">Parameters</span></span>

<span data-ttu-id="68050-358">node</span><span class="sxs-lookup"><span data-stu-id="68050-358">node</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="68050-359">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="68050-359">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="68050-360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-360">Parameters</span></span>

<span data-ttu-id="68050-361">node</span><span class="sxs-lookup"><span data-stu-id="68050-361">node</span></span>  

<!-- -->

<span data-ttu-id="68050-362">aotPath</span><span class="sxs-lookup"><span data-stu-id="68050-362">aotPath</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="68050-363">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="68050-363">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="68050-364">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-364">Parameters</span></span>

<span data-ttu-id="68050-365">データ</span><span class="sxs-lookup"><span data-stu-id="68050-365">data</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="68050-366">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="68050-366">Method AOTsetSource</span></span>

<span data-ttu-id="68050-367">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-367">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="68050-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-368">Parameters</span></span>

<span data-ttu-id="68050-369">ソース</span><span class="sxs-lookup"><span data-stu-id="68050-369">source</span></span>  
<span data-ttu-id="68050-370">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-370">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="68050-371">isStatic</span><span class="sxs-lookup"><span data-stu-id="68050-371">isStatic</span></span>  
<span data-ttu-id="68050-372">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-372">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-373">備考</span><span class="sxs-lookup"><span data-stu-id="68050-373">Remarks</span></span>

<span data-ttu-id="68050-374">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="68050-374">This method is overridden by nodes that have source code.</span></span>

### <a name="method-getfile"></a><span data-ttu-id="68050-375">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="68050-375">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-376">Parameters</span></span>

<span data-ttu-id="68050-377">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-377">fileName</span></span>  

### <a name="method-notifyfilecreated"></a><span data-ttu-id="68050-378">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="68050-378">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-379">Parameters</span></span>

<span data-ttu-id="68050-380">node</span><span class="sxs-lookup"><span data-stu-id="68050-380">node</span></span>  

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="68050-381">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="68050-381">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="68050-382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-382">Parameters</span></span>

<span data-ttu-id="68050-383">node</span><span class="sxs-lookup"><span data-stu-id="68050-383">node</span></span>  

<!-- -->

<span data-ttu-id="68050-384">oldName</span><span class="sxs-lookup"><span data-stu-id="68050-384">oldName</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="68050-385">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="68050-385">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-386">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-386">Parameters</span></span>

<span data-ttu-id="68050-387">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-387">fileName</span></span>  

## <a name="class-vsprojectlinknode"></a><span data-ttu-id="68050-388">クラス VSProjectLinkNode</span><span class="sxs-lookup"><span data-stu-id="68050-388">Class VSProjectLinkNode</span></span>
    class VSProjectLinkNode extends VSItemNode

<span data-ttu-id="68050-389">VSProjectLinkNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードにある別の Finance and Operations AOT へのリンクを表します。</span><span class="sxs-lookup"><span data-stu-id="68050-389">The VSProjectLinkNode class represents links to other Finance and Operations Application Object Tree (AOT) nodes in the Microsoft Visual Studio project nodes in the AOT.</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-390">備考</span><span class="sxs-lookup"><span data-stu-id="68050-390">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-391">例</span><span class="sxs-lookup"><span data-stu-id="68050-391">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-392">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-392">Methods</span></span>

| <span data-ttu-id="68050-393">方法</span><span class="sxs-lookup"><span data-stu-id="68050-393">Method</span></span>                                                             | <span data-ttu-id="68050-394">説明</span><span class="sxs-lookup"><span data-stu-id="68050-394">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="68050-395">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="68050-395">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="68050-396">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-396">Returns the source code of this node.</span></span> |
| <span data-ttu-id="68050-397">public str getAOTPath()</span><span class="sxs-lookup"><span data-stu-id="68050-397">public str getAOTPath()</span></span>                                            |                                       |
| <span data-ttu-id="68050-398">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="68050-398">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="68050-399">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-399">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="68050-400">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-400">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="68050-401">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="68050-401">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="68050-402">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="68050-402">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="68050-403">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="68050-403">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="68050-404">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="68050-404">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="68050-405">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-405">Sets the source code of this node.</span></span>    |
| <span data-ttu-id="68050-406">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="68050-406">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="68050-407">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="68050-407">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |

### <a name="method-aotgetsource"></a><span data-ttu-id="68050-408">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="68050-408">Method AOTgetSource</span></span>

<span data-ttu-id="68050-409">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="68050-409">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="68050-410">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-410">Return Value</span></span>

<span data-ttu-id="68050-411">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="68050-411">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-412">備考</span><span class="sxs-lookup"><span data-stu-id="68050-412">Remarks</span></span>

<span data-ttu-id="68050-413">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="68050-413">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getaotpath"></a><span data-ttu-id="68050-414">メソッド getAOTPath</span><span class="sxs-lookup"><span data-stu-id="68050-414">Method getAOTPath</span></span>

    public str getAOTPath()

#### <a name="return-value"></a><span data-ttu-id="68050-415">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-415">Return Value</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="68050-416">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="68050-416">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="68050-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-417">Return Value</span></span>

### <a name="method-notifyfilecreated"></a><span data-ttu-id="68050-418">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="68050-418">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-419">Parameters</span></span>

<span data-ttu-id="68050-420">node</span><span class="sxs-lookup"><span data-stu-id="68050-420">node</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="68050-421">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="68050-421">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-422">Parameters</span></span>

<span data-ttu-id="68050-423">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-423">fileName</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="68050-424">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="68050-424">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="68050-425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-425">Parameters</span></span>

<span data-ttu-id="68050-426">データ</span><span class="sxs-lookup"><span data-stu-id="68050-426">data</span></span>  

### <a name="method-getfile"></a><span data-ttu-id="68050-427">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="68050-427">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="68050-428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-428">Parameters</span></span>

<span data-ttu-id="68050-429">fileName</span><span class="sxs-lookup"><span data-stu-id="68050-429">fileName</span></span>  

### <a name="method-notifyfileupdated"></a><span data-ttu-id="68050-430">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="68050-430">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="68050-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-431">Parameters</span></span>

<span data-ttu-id="68050-432">node</span><span class="sxs-lookup"><span data-stu-id="68050-432">node</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="68050-433">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="68050-433">Method AOTsetSource</span></span>

<span data-ttu-id="68050-434">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-434">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="68050-435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-435">Parameters</span></span>

<span data-ttu-id="68050-436">ソース</span><span class="sxs-lookup"><span data-stu-id="68050-436">source</span></span>  
<span data-ttu-id="68050-437">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-437">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="68050-438">isStatic</span><span class="sxs-lookup"><span data-stu-id="68050-438">isStatic</span></span>  
<span data-ttu-id="68050-439">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="68050-439">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-440">備考</span><span class="sxs-lookup"><span data-stu-id="68050-440">Remarks</span></span>

<span data-ttu-id="68050-441">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="68050-441">This method is overridden by nodes that have source code.</span></span>

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="68050-442">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="68050-442">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="68050-443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-443">Parameters</span></span>

<span data-ttu-id="68050-444">node</span><span class="sxs-lookup"><span data-stu-id="68050-444">node</span></span>  

<!-- -->

<span data-ttu-id="68050-445">oldName</span><span class="sxs-lookup"><span data-stu-id="68050-445">oldName</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="68050-446">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="68050-446">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="68050-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-447">Parameters</span></span>

<span data-ttu-id="68050-448">node</span><span class="sxs-lookup"><span data-stu-id="68050-448">node</span></span>  

<!-- -->

<span data-ttu-id="68050-449">aotPath</span><span class="sxs-lookup"><span data-stu-id="68050-449">aotPath</span></span>  

## <a name="class-vsprojectnode"></a><span data-ttu-id="68050-450">クラス VSProjectNode</span><span class="sxs-lookup"><span data-stu-id="68050-450">Class VSProjectNode</span></span>
    class VSProjectNode extends xResourceNode

<span data-ttu-id="68050-451">VSProjectNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでプロジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="68050-451">The VSProjectNode class represents projects in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-452">備考</span><span class="sxs-lookup"><span data-stu-id="68050-452">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-453">例</span><span class="sxs-lookup"><span data-stu-id="68050-453">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-454">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-454">Methods</span></span>

| <span data-ttu-id="68050-455">方法</span><span class="sxs-lookup"><span data-stu-id="68050-455">Method</span></span>                                                                | <span data-ttu-id="68050-456">説明</span><span class="sxs-lookup"><span data-stu-id="68050-456">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68050-457">public container extract(\[str path\], \[boolean extractReferenced\])</span><span class="sxs-lookup"><span data-stu-id="68050-457">public container extract(\[str path\], \[boolean extractReferenced\])</span></span> | <span data-ttu-id="68050-458">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="68050-458">Extracts the whole project to disk.</span></span>                                                               |
| <span data-ttu-id="68050-459">public VSProjectFolderNode getContentNode()</span><span class="sxs-lookup"><span data-stu-id="68050-459">public VSProjectFolderNode getContentNode()</span></span>                           | <span data-ttu-id="68050-460">Visual Studio プロジェクト ファイルが格納されているコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-460">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>        |
| <span data-ttu-id="68050-461">public DeployTo getDeployTo()</span><span class="sxs-lookup"><span data-stu-id="68050-461">public DeployTo getDeployTo()</span></span>                                         | <span data-ttu-id="68050-462">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-462">Gets value of the deployTo property.</span></span>                                                              |
| <span data-ttu-id="68050-463">public VSProjectFolderNode getOutputNode()</span><span class="sxs-lookup"><span data-stu-id="68050-463">public VSProjectFolderNode getOutputNode()</span></span>                            | <span data-ttu-id="68050-464">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-464">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>  |
| <span data-ttu-id="68050-465">public VSProjectFileNode getPrimaryOutputNode()</span><span class="sxs-lookup"><span data-stu-id="68050-465">public VSProjectFileNode getPrimaryOutputNode()</span></span>                       | <span data-ttu-id="68050-466">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-466">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span> |
| <span data-ttu-id="68050-467">public str getPrimaryTargetFileName()</span><span class="sxs-lookup"><span data-stu-id="68050-467">public str getPrimaryTargetFileName()</span></span>                                 | <span data-ttu-id="68050-468">Visual Studio プロジェクトの含むプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-468">Gets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="68050-469">public Map getProxies()</span><span class="sxs-lookup"><span data-stu-id="68050-469">public Map getProxies()</span></span>                                               | <span data-ttu-id="68050-470">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-470">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="68050-471">public container getProxiesContainer()</span><span class="sxs-lookup"><span data-stu-id="68050-471">public container getProxiesContainer()</span></span>                                | <span data-ttu-id="68050-472">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-472">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="68050-473">public str getReferencedProjectsInAOT()</span><span class="sxs-lookup"><span data-stu-id="68050-473">public str getReferencedProjectsInAOT()</span></span>                               | <span data-ttu-id="68050-474">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-474">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>             |
| <span data-ttu-id="68050-475">public str referencedProjects(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="68050-475">public str referencedProjects(\[str value\])</span></span>                          |                                                                                                   |
| <span data-ttu-id="68050-476">public void setPrimaryTargetFileName(str targetFileName)</span><span class="sxs-lookup"><span data-stu-id="68050-476">public void setPrimaryTargetFileName(str targetFileName)</span></span>              | <span data-ttu-id="68050-477">Visual Studio プロジェクトの含むプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-477">Sets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="68050-478">public void extractToSpecificDir(str directory)</span><span class="sxs-lookup"><span data-stu-id="68050-478">public void extractToSpecificDir(str directory)</span></span>                       |                                                                                                   |
| <span data-ttu-id="68050-479">public void setDeployTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="68050-479">public void setDeployTo(DeployTo deployTo)</span></span>                            | <span data-ttu-id="68050-480">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-480">Sets the value of the deployTo property.</span></span>                                                          |

### <a name="method-extract"></a><span data-ttu-id="68050-481">メソッド extract</span><span class="sxs-lookup"><span data-stu-id="68050-481">Method extract</span></span>

<span data-ttu-id="68050-482">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="68050-482">Extracts the whole project to disk.</span></span>

    public container extract([str path], [boolean extractReferenced])

#### <a name="parameters"></a><span data-ttu-id="68050-483">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-483">Parameters</span></span>

<span data-ttu-id="68050-484">path</span><span class="sxs-lookup"><span data-stu-id="68050-484">path</span></span>  
<span data-ttu-id="68050-485">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="68050-485">A Boolean value that determines whether to extract the referenced projects.</span></span>

<!-- -->

<span data-ttu-id="68050-486">extractReferenced</span><span class="sxs-lookup"><span data-stu-id="68050-486">extractReferenced</span></span>  
<span data-ttu-id="68050-487">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="68050-487">A Boolean value that determines whether to extract the referenced projects.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-488">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-488">Return Value</span></span>

<span data-ttu-id="68050-489">プロジェクトの展開先のパスの一覧。</span><span class="sxs-lookup"><span data-stu-id="68050-489">A list of paths where the project was extracted.</span></span>

### <a name="method-getcontentnode"></a><span data-ttu-id="68050-490">メソッド getContentNode</span><span class="sxs-lookup"><span data-stu-id="68050-490">Method getContentNode</span></span>

<span data-ttu-id="68050-491">Visual Studio プロジェクト ファイルが格納されているコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-491">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

    public VSProjectFolderNode getContentNode()

#### <a name="return-value"></a><span data-ttu-id="68050-492">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-492">Return Value</span></span>

<span data-ttu-id="68050-493">Visual Studio プロジェクト ファイルが格納されているコンテンツの VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="68050-493">The content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

### <a name="method-getdeployto"></a><span data-ttu-id="68050-494">メソッド getDeployTo</span><span class="sxs-lookup"><span data-stu-id="68050-494">Method getDeployTo</span></span>

<span data-ttu-id="68050-495">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-495">Gets value of the deployTo property.</span></span>

    public DeployTo getDeployTo()

#### <a name="return-value"></a><span data-ttu-id="68050-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-496">Return Value</span></span>

<span data-ttu-id="68050-497">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="68050-497">The deployTo property value.</span></span>

### <a name="method-getoutputnode"></a><span data-ttu-id="68050-498">メソッド getOutputNode</span><span class="sxs-lookup"><span data-stu-id="68050-498">Method getOutputNode</span></span>

<span data-ttu-id="68050-499">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-499">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

    public VSProjectFolderNode getOutputNode()

#### <a name="return-value"></a><span data-ttu-id="68050-500">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-500">Return Value</span></span>

<span data-ttu-id="68050-501">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="68050-501">The output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

### <a name="method-getprimaryoutputnode"></a><span data-ttu-id="68050-502">メソッド getPrimaryOutputNode</span><span class="sxs-lookup"><span data-stu-id="68050-502">Method getPrimaryOutputNode</span></span>

<span data-ttu-id="68050-503">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-503">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

    public VSProjectFileNode getPrimaryOutputNode()

#### <a name="return-value"></a><span data-ttu-id="68050-504">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-504">Return Value</span></span>

<span data-ttu-id="68050-505">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="68050-505">A VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

### <a name="method-getprimarytargetfilename"></a><span data-ttu-id="68050-506">メソッド getPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="68050-506">Method getPrimaryTargetFileName</span></span>

<span data-ttu-id="68050-507">Visual Studio プロジェクトの含むプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-507">Gets the primary target file name of the Visual Studio project.</span></span>

    public str getPrimaryTargetFileName()

#### <a name="return-value"></a><span data-ttu-id="68050-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-508">Return Value</span></span>

<span data-ttu-id="68050-509">Visual Studio プロジェクトの含むプライマリ ターゲット ファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="68050-509">The primary target file name of the Visual Studio project.</span></span>

### <a name="method-getproxies"></a><span data-ttu-id="68050-510">メソッド getProxies</span><span class="sxs-lookup"><span data-stu-id="68050-510">Method getProxies</span></span>

<span data-ttu-id="68050-511">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-511">Gets the proxies in this project.</span></span>

    public Map getProxies()

#### <a name="return-value"></a><span data-ttu-id="68050-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-512">Return Value</span></span>

<span data-ttu-id="68050-513">クラス、列挙、およびテーブルのキーを含むマップ。</span><span class="sxs-lookup"><span data-stu-id="68050-513">A map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="68050-514">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68050-514">Each key contains a list of proxies.</span></span>

### <a name="method-getproxiescontainer"></a><span data-ttu-id="68050-515">メソッド getProxiesContainer</span><span class="sxs-lookup"><span data-stu-id="68050-515">Method getProxiesContainer</span></span>

<span data-ttu-id="68050-516">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-516">Gets the proxies in this project.</span></span>

    public container getProxiesContainer()

#### <a name="return-value"></a><span data-ttu-id="68050-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-517">Return Value</span></span>

<span data-ttu-id="68050-518">マップの梱包済み表現を保持するコンテナーには、Class、Enum、Table のキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68050-518">A container that holds the packed representation of a map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="68050-519">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68050-519">Each key contains a list of proxies.</span></span>

### <a name="method-getreferencedprojectsinaot"></a><span data-ttu-id="68050-520">メソッド getReferencedProjectsInAOT</span><span class="sxs-lookup"><span data-stu-id="68050-520">Method getReferencedProjectsInAOT</span></span>

<span data-ttu-id="68050-521">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-521">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

    public str getReferencedProjectsInAOT()

#### <a name="return-value"></a><span data-ttu-id="68050-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-522">Return Value</span></span>

<span data-ttu-id="68050-523">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスの一覧。</span><span class="sxs-lookup"><span data-stu-id="68050-523">A list of AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

### <a name="method-referencedprojects"></a><span data-ttu-id="68050-524">メソッド referencedProjects</span><span class="sxs-lookup"><span data-stu-id="68050-524">Method referencedProjects</span></span>

    public str referencedProjects([str value])

#### <a name="parameters"></a><span data-ttu-id="68050-525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-525">Parameters</span></span>

<span data-ttu-id="68050-526">値</span><span class="sxs-lookup"><span data-stu-id="68050-526">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-527">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-527">Return Value</span></span>

### <a name="method-setprimarytargetfilename"></a><span data-ttu-id="68050-528">メソッド setPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="68050-528">Method setPrimaryTargetFileName</span></span>

<span data-ttu-id="68050-529">Visual Studio プロジェクトの含むプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-529">Sets the primary target file name of the Visual Studio project.</span></span>

    public void setPrimaryTargetFileName(str targetFileName)

#### <a name="parameters"></a><span data-ttu-id="68050-530">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-530">Parameters</span></span>

<span data-ttu-id="68050-531">targetFileName</span><span class="sxs-lookup"><span data-stu-id="68050-531">targetFileName</span></span>  
<span data-ttu-id="68050-532">Visual Studio プロジェクトの含むプライマリ ターゲット ファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="68050-532">The primary target file name of the Visual Studio project.</span></span>

### <a name="method-extracttospecificdir"></a><span data-ttu-id="68050-533">メソッド extractToSpecificDir</span><span class="sxs-lookup"><span data-stu-id="68050-533">Method extractToSpecificDir</span></span>

    public void extractToSpecificDir(str directory)

#### <a name="parameters"></a><span data-ttu-id="68050-534">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-534">Parameters</span></span>

<span data-ttu-id="68050-535">directory</span><span class="sxs-lookup"><span data-stu-id="68050-535">directory</span></span>  

### <a name="method-setdeployto"></a><span data-ttu-id="68050-536">メソッド setDeployTo</span><span class="sxs-lookup"><span data-stu-id="68050-536">Method setDeployTo</span></span>

<span data-ttu-id="68050-537">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="68050-537">Sets the value of the deployTo property.</span></span>

    public void setDeployTo(DeployTo deployTo)

#### <a name="parameters"></a><span data-ttu-id="68050-538">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-538">Parameters</span></span>

<span data-ttu-id="68050-539">deployTo</span><span class="sxs-lookup"><span data-stu-id="68050-539">deployTo</span></span>  
<span data-ttu-id="68050-540">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="68050-540">The deployTo property value.</span></span>

## <a name="class-vsprojectsnode"></a><span data-ttu-id="68050-541">クラス VSProjectsNode</span><span class="sxs-lookup"><span data-stu-id="68050-541">Class VSProjectsNode</span></span>
    class VSProjectsNode extends xResourceNode

<span data-ttu-id="68050-542">VSProjectNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードのルートです。</span><span class="sxs-lookup"><span data-stu-id="68050-542">The VSProjectNode class is the root of the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-543">備考</span><span class="sxs-lookup"><span data-stu-id="68050-543">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-544">例</span><span class="sxs-lookup"><span data-stu-id="68050-544">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-545">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-545">Methods</span></span>

| <span data-ttu-id="68050-546">方法</span><span class="sxs-lookup"><span data-stu-id="68050-546">Method</span></span>                                                                                            | <span data-ttu-id="68050-547">説明</span><span class="sxs-lookup"><span data-stu-id="68050-547">Description</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="68050-548">public TreeNode AOTfindChild(str name, \[int nodeType\])</span><span class="sxs-lookup"><span data-stu-id="68050-548">public TreeNode AOTfindChild(str name, \[int nodeType\])</span></span>                                          | <span data-ttu-id="68050-549">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="68050-549">Finds the specified child node of this node.</span></span>                                               |
| <span data-ttu-id="68050-550">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span><span class="sxs-lookup"><span data-stu-id="68050-550">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span></span> | <span data-ttu-id="68050-551">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-551">Creates a new instance of the VSProjectNode class.</span></span>                                         |
| <span data-ttu-id="68050-552">public container getProjectsDeployingTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="68050-552">public container getProjectsDeployingTo(DeployTo deployTo)</span></span>                                        | <span data-ttu-id="68050-553">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-553">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>            |
| <span data-ttu-id="68050-554">public container getProjectsModifiedAfter(DateTime timestamp)</span><span class="sxs-lookup"><span data-stu-id="68050-554">public container getProjectsModifiedAfter(DateTime timestamp)</span></span>                                     | <span data-ttu-id="68050-555">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-555">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span> |
| <span data-ttu-id="68050-556">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span><span class="sxs-lookup"><span data-stu-id="68050-556">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span></span>                              |                                                                                            |
| <span data-ttu-id="68050-557">public Object getVSProjectNodeObservable()</span><span class="sxs-lookup"><span data-stu-id="68050-557">public Object getVSProjectNodeObservable()</span></span>                                                        | <span data-ttu-id="68050-558">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-558">Gets the VSProjectNodeObservable object.</span></span>                                                   |
| <span data-ttu-id="68050-559">public void AOTrefresh()</span><span class="sxs-lookup"><span data-stu-id="68050-559">public void AOTrefresh()</span></span>                                                                          | <span data-ttu-id="68050-560">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="68050-560">Updates the node with the latest changes to the .aod file.</span></span>                                 |

### <a name="method-aotfindchild"></a><span data-ttu-id="68050-561">メソッド AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="68050-561">Method AOTfindChild</span></span>

<span data-ttu-id="68050-562">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="68050-562">Finds the specified child node of this node.</span></span>

    public TreeNode AOTfindChild(str name, [int nodeType])

#### <a name="parameters"></a><span data-ttu-id="68050-563">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-563">Parameters</span></span>

<span data-ttu-id="68050-564">名前</span><span class="sxs-lookup"><span data-stu-id="68050-564">name</span></span>  

<!-- -->

<span data-ttu-id="68050-565">nodeType</span><span class="sxs-lookup"><span data-stu-id="68050-565">nodeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-566">Return Value</span></span>

<span data-ttu-id="68050-567">指定したツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="68050-567">The specified tree node.</span></span>

### <a name="method-createprojectnode"></a><span data-ttu-id="68050-568">メソッド createProjectNode</span><span class="sxs-lookup"><span data-stu-id="68050-568">Method createProjectNode</span></span>

<span data-ttu-id="68050-569">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68050-569">Creates a new instance of the VSProjectNode class.</span></span>

    public VSProjectNode createProjectNode(str name, str projectTypesString, [boolean virtualNode])

#### <a name="parameters"></a><span data-ttu-id="68050-570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-570">Parameters</span></span>

<span data-ttu-id="68050-571">名前</span><span class="sxs-lookup"><span data-stu-id="68050-571">name</span></span>  
<span data-ttu-id="68050-572">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="68050-572">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="68050-573">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="68050-573">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="68050-574">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="68050-574">projectTypesString</span></span>  
<span data-ttu-id="68050-575">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="68050-575">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="68050-576">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="68050-576">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="68050-577">virtualNode</span><span class="sxs-lookup"><span data-stu-id="68050-577">virtualNode</span></span>  
<span data-ttu-id="68050-578">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="68050-578">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="68050-579">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="68050-579">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-580">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-580">Return Value</span></span>

<span data-ttu-id="68050-581">作成された VSProjectNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="68050-581">The VSProjectNode object that is created.</span></span>

### <a name="method-getprojectsdeployingto"></a><span data-ttu-id="68050-582">メソッド getProjectsDeployingTo</span><span class="sxs-lookup"><span data-stu-id="68050-582">Method getProjectsDeployingTo</span></span>

<span data-ttu-id="68050-583">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-583">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>

    public container getProjectsDeployingTo(DeployTo deployTo)

#### <a name="parameters"></a><span data-ttu-id="68050-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-584">Parameters</span></span>

<span data-ttu-id="68050-585">deployTo</span><span class="sxs-lookup"><span data-stu-id="68050-585">deployTo</span></span>  
<span data-ttu-id="68050-586">deployTo プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="68050-586">The value of the deployTo property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-587">Return Value</span></span>

<span data-ttu-id="68050-588">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="68050-588">A list of VSProjectNode objects.</span></span>

### <a name="method-getprojectsmodifiedafter"></a><span data-ttu-id="68050-589">メソッド getProjectsModifiedAfter</span><span class="sxs-lookup"><span data-stu-id="68050-589">Method getProjectsModifiedAfter</span></span>

<span data-ttu-id="68050-590">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-590">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span>

    public container getProjectsModifiedAfter(DateTime timestamp)

#### <a name="parameters"></a><span data-ttu-id="68050-591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-591">Parameters</span></span>

<span data-ttu-id="68050-592">timestamp</span><span class="sxs-lookup"><span data-stu-id="68050-592">timestamp</span></span>  
<span data-ttu-id="68050-593">DB\_DATETIME\_TYPE 値としての日時。</span><span class="sxs-lookup"><span data-stu-id="68050-593">The date and time as a DB\_DATETIME\_TYPE value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="68050-594">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-594">Return Value</span></span>

<span data-ttu-id="68050-595">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="68050-595">A list of VSProjectNode objects.</span></span>

### <a name="method-gettypenodefromguid"></a><span data-ttu-id="68050-596">メソッド getTypeNodeFromGuid</span><span class="sxs-lookup"><span data-stu-id="68050-596">Method getTypeNodeFromGuid</span></span>

    public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)

#### <a name="parameters"></a><span data-ttu-id="68050-597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-597">Parameters</span></span>

<span data-ttu-id="68050-598">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="68050-598">projectTypesString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-599">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-599">Return Value</span></span>

### <a name="method-getvsprojectnodeobservable"></a><span data-ttu-id="68050-600">メソッド getVSProjectNodeObservable</span><span class="sxs-lookup"><span data-stu-id="68050-600">Method getVSProjectNodeObservable</span></span>

<span data-ttu-id="68050-601">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="68050-601">Gets the VSProjectNodeObservable object.</span></span>

    public Object getVSProjectNodeObservable()

#### <a name="return-value"></a><span data-ttu-id="68050-602">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-602">Return Value</span></span>

<span data-ttu-id="68050-603">VSProjectNodeObservable オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="68050-603">The VSProjectNodeObservable object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="68050-604">備考</span><span class="sxs-lookup"><span data-stu-id="68050-604">Remarks</span></span>

<span data-ttu-id="68050-605">オブザーバーはこれで登録でき、Visual Studio プロジェクトで CRUD 操作の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="68050-605">Observers can register with this and get notified of CRUD operations on Visual Studio projects.</span></span>

### <a name="method-aotrefresh"></a><span data-ttu-id="68050-606">メソッド AOTrefresh</span><span class="sxs-lookup"><span data-stu-id="68050-606">Method AOTrefresh</span></span>

<span data-ttu-id="68050-607">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="68050-607">Updates the node with the latest changes to the .aod file.</span></span>

    public void AOTrefresh()

## <a name="class-vsprojecttypenode"></a><span data-ttu-id="68050-608">クラス VSProjectTypeNode</span><span class="sxs-lookup"><span data-stu-id="68050-608">Class VSProjectTypeNode</span></span>
    class VSProjectTypeNode extends TreeNode

<span data-ttu-id="68050-609">VSProjectTypeNode クラスは、AOT 内の Visual Studio プロジェクト ノードでプロジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="68050-609">The VSProjectTypeNode class represents project types in the Visual Studio Project nodes in the AOT.</span></span>

### <a name="remarks"></a><span data-ttu-id="68050-610">備考</span><span class="sxs-lookup"><span data-stu-id="68050-610">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-611">例</span><span class="sxs-lookup"><span data-stu-id="68050-611">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-612">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-612">Methods</span></span>

| <span data-ttu-id="68050-613">方法</span><span class="sxs-lookup"><span data-stu-id="68050-613">Method</span></span> | <span data-ttu-id="68050-614">説明</span><span class="sxs-lookup"><span data-stu-id="68050-614">Description</span></span> |
|--------|-------------|
|        |             |

## <a name="class-vss"></a><span data-ttu-id="68050-615">クラス VSS</span><span class="sxs-lookup"><span data-stu-id="68050-615">Class VSS</span></span>
    class VSS extends Object

### <a name="remarks"></a><span data-ttu-id="68050-616">備考</span><span class="sxs-lookup"><span data-stu-id="68050-616">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-617">例</span><span class="sxs-lookup"><span data-stu-id="68050-617">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-618">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-618">Methods</span></span>

| <span data-ttu-id="68050-619">方法</span><span class="sxs-lookup"><span data-stu-id="68050-619">Method</span></span>                                                                                                        | <span data-ttu-id="68050-620">説明</span><span class="sxs-lookup"><span data-stu-id="68050-620">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="68050-621">public boolean connect()</span><span class="sxs-lookup"><span data-stu-id="68050-621">public boolean connect()</span></span>                                                                                      |                                           |
| <span data-ttu-id="68050-622">public boolean connected()</span><span class="sxs-lookup"><span data-stu-id="68050-622">public boolean connected()</span></span>                                                                                    |                                           |
| <span data-ttu-id="68050-623">public boolean disconnect()</span><span class="sxs-lookup"><span data-stu-id="68050-623">public boolean disconnect()</span></span>                                                                                   |                                           |
| <span data-ttu-id="68050-624">public container getCheckedoutFiles()</span><span class="sxs-lookup"><span data-stu-id="68050-624">public container getCheckedoutFiles()</span></span>                                                                         |                                           |
| <span data-ttu-id="68050-625">public container getConnectionInfo()</span><span class="sxs-lookup"><span data-stu-id="68050-625">public container getConnectionInfo()</span></span>                                                                          |                                           |
| <span data-ttu-id="68050-626">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span><span class="sxs-lookup"><span data-stu-id="68050-626">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span></span>      |                                           |
| <span data-ttu-id="68050-627">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span><span class="sxs-lookup"><span data-stu-id="68050-627">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span></span>                |                                           |
| <span data-ttu-id="68050-628">public VSSItem newSubProject(str name, str localPath)</span><span class="sxs-lookup"><span data-stu-id="68050-628">public VSSItem newSubProject(str name, str localPath)</span></span>                                                         |                                           |
| <span data-ttu-id="68050-629">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span><span class="sxs-lookup"><span data-stu-id="68050-629">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span></span> |                                           |
| <span data-ttu-id="68050-630">public void new()</span><span class="sxs-lookup"><span data-stu-id="68050-630">public void new()</span></span>                                                                                             | <span data-ttu-id="68050-631">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-631">Initializes an instance of the VSS class.</span></span> |

### <a name="method-connect"></a><span data-ttu-id="68050-632">メソッド connect</span><span class="sxs-lookup"><span data-stu-id="68050-632">Method connect</span></span>

    public boolean connect()

#### <a name="return-value"></a><span data-ttu-id="68050-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-633">Return Value</span></span>

### <a name="method-connected"></a><span data-ttu-id="68050-634">メソッド connected</span><span class="sxs-lookup"><span data-stu-id="68050-634">Method connected</span></span>

    public boolean connected()

#### <a name="return-value"></a><span data-ttu-id="68050-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-635">Return Value</span></span>

### <a name="method-disconnect"></a><span data-ttu-id="68050-636">メソッド disconnect</span><span class="sxs-lookup"><span data-stu-id="68050-636">Method disconnect</span></span>

    public boolean disconnect()

#### <a name="return-value"></a><span data-ttu-id="68050-637">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-637">Return Value</span></span>

### <a name="method-getcheckedoutfiles"></a><span data-ttu-id="68050-638">メソッド getCheckedoutFiles</span><span class="sxs-lookup"><span data-stu-id="68050-638">Method getCheckedoutFiles</span></span>

    public container getCheckedoutFiles()

#### <a name="return-value"></a><span data-ttu-id="68050-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-639">Return Value</span></span>

### <a name="method-getconnectioninfo"></a><span data-ttu-id="68050-640">メソッド getConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="68050-640">Method getConnectionInfo</span></span>

    public container getConnectionInfo()

#### <a name="return-value"></a><span data-ttu-id="68050-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-641">Return Value</span></span>

### <a name="method-getvssitem"></a><span data-ttu-id="68050-642">メソッド getVSSItem</span><span class="sxs-lookup"><span data-stu-id="68050-642">Method getVSSItem</span></span>

    public VSSItem getVSSItem(str vssItemPath, str localFilePath, [boolean completePath], [int version])

#### <a name="parameters"></a><span data-ttu-id="68050-643">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-643">Parameters</span></span>

<span data-ttu-id="68050-644">vssItemPath</span><span class="sxs-lookup"><span data-stu-id="68050-644">vssItemPath</span></span>  

<!-- -->

<span data-ttu-id="68050-645">localFilePath</span><span class="sxs-lookup"><span data-stu-id="68050-645">localFilePath</span></span>  

<!-- -->

<span data-ttu-id="68050-646">completePath</span><span class="sxs-lookup"><span data-stu-id="68050-646">completePath</span></span>  

<!-- -->

<span data-ttu-id="68050-647">のバージョン</span><span class="sxs-lookup"><span data-stu-id="68050-647">version</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-648">Return Value</span></span>

### <a name="method-init"></a><span data-ttu-id="68050-649">メソッド init</span><span class="sxs-lookup"><span data-stu-id="68050-649">Method init</span></span>

    public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)

#### <a name="parameters"></a><span data-ttu-id="68050-650">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-650">Parameters</span></span>

<span data-ttu-id="68050-651">vssIni</span><span class="sxs-lookup"><span data-stu-id="68050-651">vssIni</span></span>  

<!-- -->

<span data-ttu-id="68050-652">vssPrjRoot</span><span class="sxs-lookup"><span data-stu-id="68050-652">vssPrjRoot</span></span>  

<!-- -->

<span data-ttu-id="68050-653">vssWorkingFolder</span><span class="sxs-lookup"><span data-stu-id="68050-653">vssWorkingFolder</span></span>  

<!-- -->

<span data-ttu-id="68050-654">vssUser</span><span class="sxs-lookup"><span data-stu-id="68050-654">vssUser</span></span>  

<!-- -->

<span data-ttu-id="68050-655">vssPwd</span><span class="sxs-lookup"><span data-stu-id="68050-655">vssPwd</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-656">Return Value</span></span>

### <a name="method-newsubproject"></a><span data-ttu-id="68050-657">メソッド newSubProject</span><span class="sxs-lookup"><span data-stu-id="68050-657">Method newSubProject</span></span>

    public VSSItem newSubProject(str name, str localPath)

#### <a name="parameters"></a><span data-ttu-id="68050-658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-658">Parameters</span></span>

<span data-ttu-id="68050-659">名前</span><span class="sxs-lookup"><span data-stu-id="68050-659">name</span></span>  

<!-- -->

<span data-ttu-id="68050-660">localPath</span><span class="sxs-lookup"><span data-stu-id="68050-660">localPath</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-661">Return Value</span></span>

### <a name="method-synchronizeprojects"></a><span data-ttu-id="68050-662">メソッド synchronizeProjects</span><span class="sxs-lookup"><span data-stu-id="68050-662">Method synchronizeProjects</span></span>

    public Map synchronizeProjects([Set projects], [boolean force], [boolean delLocalFiles], [str label])

#### <a name="parameters"></a><span data-ttu-id="68050-663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-663">Parameters</span></span>

<span data-ttu-id="68050-664">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="68050-664">projects</span></span>  

<!-- -->

<span data-ttu-id="68050-665">force</span><span class="sxs-lookup"><span data-stu-id="68050-665">force</span></span>  

<!-- -->

<span data-ttu-id="68050-666">delLocalFiles</span><span class="sxs-lookup"><span data-stu-id="68050-666">delLocalFiles</span></span>  

<!-- -->

<span data-ttu-id="68050-667">ラベル</span><span class="sxs-lookup"><span data-stu-id="68050-667">label</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-668">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-668">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="68050-669">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-669">Method new</span></span>

<span data-ttu-id="68050-670">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-670">Initializes an instance of the VSS class.</span></span>

    public void new()

## <a name="class-vssitem"></a><span data-ttu-id="68050-671">クラス VSSItem</span><span class="sxs-lookup"><span data-stu-id="68050-671">Class VSSItem</span></span>
    class VSSItem extends Object

### <a name="remarks"></a><span data-ttu-id="68050-672">備考</span><span class="sxs-lookup"><span data-stu-id="68050-672">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68050-673">例</span><span class="sxs-lookup"><span data-stu-id="68050-673">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="68050-674">メソッド</span><span class="sxs-lookup"><span data-stu-id="68050-674">Methods</span></span>

| <span data-ttu-id="68050-675">方法</span><span class="sxs-lookup"><span data-stu-id="68050-675">Method</span></span>                                                                               | <span data-ttu-id="68050-676">説明</span><span class="sxs-lookup"><span data-stu-id="68050-676">Description</span></span>                                      |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="68050-677">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="68050-677">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span></span>                      |                                                  |
| <span data-ttu-id="68050-678">public boolean checkin(\[str comment\])</span><span class="sxs-lookup"><span data-stu-id="68050-678">public boolean checkin(\[str comment\])</span></span>                                              |                                                  |
| <span data-ttu-id="68050-679">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span><span class="sxs-lookup"><span data-stu-id="68050-679">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span></span> |                                                  |
| <span data-ttu-id="68050-680">public boolean delete()</span><span class="sxs-lookup"><span data-stu-id="68050-680">public boolean delete()</span></span>                                                              |                                                  |
| <span data-ttu-id="68050-681">public boolean destroy()</span><span class="sxs-lookup"><span data-stu-id="68050-681">public boolean destroy()</span></span>                                                             |                                                  |
| <span data-ttu-id="68050-682">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span><span class="sxs-lookup"><span data-stu-id="68050-682">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span></span> |                                                  |
| <span data-ttu-id="68050-683">public str getActionText()</span><span class="sxs-lookup"><span data-stu-id="68050-683">public str getActionText()</span></span>                                                           |                                                  |
| <span data-ttu-id="68050-684">public container getCheckedOutTo()</span><span class="sxs-lookup"><span data-stu-id="68050-684">public container getCheckedOutTo()</span></span>                                                   |                                                  |
| <span data-ttu-id="68050-685">public int getCheckoutVersion()</span><span class="sxs-lookup"><span data-stu-id="68050-685">public int getCheckoutVersion()</span></span>                                                      |                                                  |
| <span data-ttu-id="68050-686">public container getHistory()</span><span class="sxs-lookup"><span data-stu-id="68050-686">public container getHistory()</span></span>                                                        |                                                  |
| <span data-ttu-id="68050-687">public ComInterface getIUnknown()</span><span class="sxs-lookup"><span data-stu-id="68050-687">public ComInterface getIUnknown()</span></span>                                                    |                                                  |
| <span data-ttu-id="68050-688">public int getVersionNo()</span><span class="sxs-lookup"><span data-stu-id="68050-688">public int getVersionNo()</span></span>                                                            |                                                  |
| <span data-ttu-id="68050-689">public str getVSSPath()</span><span class="sxs-lookup"><span data-stu-id="68050-689">public str getVSSPath()</span></span>                                                              |                                                  |
| <span data-ttu-id="68050-690">public boolean isCheckedOut()</span><span class="sxs-lookup"><span data-stu-id="68050-690">public boolean isCheckedOut()</span></span>                                                        |                                                  |
| <span data-ttu-id="68050-691">public boolean isRenamed()</span><span class="sxs-lookup"><span data-stu-id="68050-691">public boolean isRenamed()</span></span>                                                           |                                                  |
| <span data-ttu-id="68050-692">public str name(str newName)</span><span class="sxs-lookup"><span data-stu-id="68050-692">public str name(str newName)</span></span>                                                         |                                                  |
| <span data-ttu-id="68050-693">public boolean rename(str newName)</span><span class="sxs-lookup"><span data-stu-id="68050-693">public boolean rename(str newName)</span></span>                                                   |                                                  |
| <span data-ttu-id="68050-694">public boolean undoCheckout()</span><span class="sxs-lookup"><span data-stu-id="68050-694">public boolean undoCheckout()</span></span>                                                        |                                                  |
| <span data-ttu-id="68050-695">private void new()</span><span class="sxs-lookup"><span data-stu-id="68050-695">private void new()</span></span>                                                                   | <span data-ttu-id="68050-696">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-696">Initializes a new instance of the VSSItem class.</span></span> |

### <a name="method-add"></a><span data-ttu-id="68050-697">メソッド add</span><span class="sxs-lookup"><span data-stu-id="68050-697">Method add</span></span>

    public boolean add([boolean keepCheckedout], [str comment])

#### <a name="parameters"></a><span data-ttu-id="68050-698">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-698">Parameters</span></span>

<span data-ttu-id="68050-699">keepCheckedout</span><span class="sxs-lookup"><span data-stu-id="68050-699">keepCheckedout</span></span>  

<!-- -->

<span data-ttu-id="68050-700">comment</span><span class="sxs-lookup"><span data-stu-id="68050-700">comment</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-701">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-701">Return Value</span></span>

### <a name="method-checkin"></a><span data-ttu-id="68050-702">メソッド checkin</span><span class="sxs-lookup"><span data-stu-id="68050-702">Method checkin</span></span>

    public boolean checkin([str comment])

#### <a name="parameters"></a><span data-ttu-id="68050-703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-703">Parameters</span></span>

<span data-ttu-id="68050-704">comment</span><span class="sxs-lookup"><span data-stu-id="68050-704">comment</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-705">Return Value</span></span>

### <a name="method-checkout"></a><span data-ttu-id="68050-706">メソッド checkout</span><span class="sxs-lookup"><span data-stu-id="68050-706">Method checkout</span></span>

    public boolean checkout([boolean allowMultipleCheckout], [boolean replaceLocal])

#### <a name="parameters"></a><span data-ttu-id="68050-707">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-707">Parameters</span></span>

<span data-ttu-id="68050-708">allowMultipleCheckout</span><span class="sxs-lookup"><span data-stu-id="68050-708">allowMultipleCheckout</span></span>  

<!-- -->

<span data-ttu-id="68050-709">replaceLocal</span><span class="sxs-lookup"><span data-stu-id="68050-709">replaceLocal</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-710">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-710">Return Value</span></span>

### <a name="method-delete"></a><span data-ttu-id="68050-711">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="68050-711">Method delete</span></span>

    public boolean delete()

#### <a name="return-value"></a><span data-ttu-id="68050-712">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-712">Return Value</span></span>

### <a name="method-destroy"></a><span data-ttu-id="68050-713">メソッド destroy</span><span class="sxs-lookup"><span data-stu-id="68050-713">Method destroy</span></span>

    public boolean destroy()

#### <a name="return-value"></a><span data-ttu-id="68050-714">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-714">Return Value</span></span>

### <a name="method-get"></a><span data-ttu-id="68050-715">メソッド get</span><span class="sxs-lookup"><span data-stu-id="68050-715">Method get</span></span>

    public Map get([boolean force], [int version], [str label], [str localFile])

#### <a name="parameters"></a><span data-ttu-id="68050-716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-716">Parameters</span></span>

<span data-ttu-id="68050-717">force</span><span class="sxs-lookup"><span data-stu-id="68050-717">force</span></span>  

<!-- -->

<span data-ttu-id="68050-718">のバージョン</span><span class="sxs-lookup"><span data-stu-id="68050-718">version</span></span>  

<!-- -->

<span data-ttu-id="68050-719">ラベル</span><span class="sxs-lookup"><span data-stu-id="68050-719">label</span></span>  

<!-- -->

<span data-ttu-id="68050-720">localFile</span><span class="sxs-lookup"><span data-stu-id="68050-720">localFile</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-721">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-721">Return Value</span></span>

### <a name="method-getactiontext"></a><span data-ttu-id="68050-722">メソッド getActionText</span><span class="sxs-lookup"><span data-stu-id="68050-722">Method getActionText</span></span>

    public str getActionText()

#### <a name="return-value"></a><span data-ttu-id="68050-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-723">Return Value</span></span>

### <a name="method-getcheckedoutto"></a><span data-ttu-id="68050-724">メソッド getCheckedOutTo</span><span class="sxs-lookup"><span data-stu-id="68050-724">Method getCheckedOutTo</span></span>

    public container getCheckedOutTo()

#### <a name="return-value"></a><span data-ttu-id="68050-725">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-725">Return Value</span></span>

### <a name="method-getcheckoutversion"></a><span data-ttu-id="68050-726">メソッド getCheckoutVersion</span><span class="sxs-lookup"><span data-stu-id="68050-726">Method getCheckoutVersion</span></span>

    public int getCheckoutVersion()

#### <a name="return-value"></a><span data-ttu-id="68050-727">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-727">Return Value</span></span>

### <a name="method-gethistory"></a><span data-ttu-id="68050-728">メソッド getHistory</span><span class="sxs-lookup"><span data-stu-id="68050-728">Method getHistory</span></span>

    public container getHistory()

#### <a name="return-value"></a><span data-ttu-id="68050-729">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-729">Return Value</span></span>

### <a name="method-getiunknown"></a><span data-ttu-id="68050-730">メソッド getIUnknown</span><span class="sxs-lookup"><span data-stu-id="68050-730">Method getIUnknown</span></span>

    public ComInterface getIUnknown()

#### <a name="return-value"></a><span data-ttu-id="68050-731">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-731">Return Value</span></span>

### <a name="method-getversionno"></a><span data-ttu-id="68050-732">メソッド getVersionNo</span><span class="sxs-lookup"><span data-stu-id="68050-732">Method getVersionNo</span></span>

    public int getVersionNo()

#### <a name="return-value"></a><span data-ttu-id="68050-733">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-733">Return Value</span></span>

### <a name="method-getvsspath"></a><span data-ttu-id="68050-734">メソッド getVSSPath</span><span class="sxs-lookup"><span data-stu-id="68050-734">Method getVSSPath</span></span>

    public str getVSSPath()

#### <a name="return-value"></a><span data-ttu-id="68050-735">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-735">Return Value</span></span>

### <a name="method-ischeckedout"></a><span data-ttu-id="68050-736">メソッド isCheckedOut</span><span class="sxs-lookup"><span data-stu-id="68050-736">Method isCheckedOut</span></span>

    public boolean isCheckedOut()

#### <a name="return-value"></a><span data-ttu-id="68050-737">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-737">Return Value</span></span>

### <a name="method-isrenamed"></a><span data-ttu-id="68050-738">メソッド isRenamed</span><span class="sxs-lookup"><span data-stu-id="68050-738">Method isRenamed</span></span>

    public boolean isRenamed()

#### <a name="return-value"></a><span data-ttu-id="68050-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-739">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="68050-740">メソッド名</span><span class="sxs-lookup"><span data-stu-id="68050-740">Method name</span></span>

    public str name(str newName)

#### <a name="parameters"></a><span data-ttu-id="68050-741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-741">Parameters</span></span>

<span data-ttu-id="68050-742">newName</span><span class="sxs-lookup"><span data-stu-id="68050-742">newName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-743">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-743">Return Value</span></span>

### <a name="method-rename"></a><span data-ttu-id="68050-744">メソッド rename</span><span class="sxs-lookup"><span data-stu-id="68050-744">Method rename</span></span>

    public boolean rename(str newName)

#### <a name="parameters"></a><span data-ttu-id="68050-745">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68050-745">Parameters</span></span>

<span data-ttu-id="68050-746">newName</span><span class="sxs-lookup"><span data-stu-id="68050-746">newName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="68050-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-747">Return Value</span></span>

### <a name="method-undocheckout"></a><span data-ttu-id="68050-748">メソッド undoCheckout</span><span class="sxs-lookup"><span data-stu-id="68050-748">Method undoCheckout</span></span>

    public boolean undoCheckout()

#### <a name="return-value"></a><span data-ttu-id="68050-749">戻り値</span><span class="sxs-lookup"><span data-stu-id="68050-749">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="68050-750">メソッド new</span><span class="sxs-lookup"><span data-stu-id="68050-750">Method new</span></span>

<span data-ttu-id="68050-751">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="68050-751">Initializes a new instance of the VSSItem class.</span></span>

    private void new()



