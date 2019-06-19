---
title: V クラス
description: 文字 V で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55841
ms.assetid: fd3859a7-c0e5-41b3-9bd3-fc68099e727f
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0bd05f773b43f8f9ca1a0a364b9810bad4feb5a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544183"
---
# <a name="v-classes"></a><span data-ttu-id="83787-103">V クラス</span><span class="sxs-lookup"><span data-stu-id="83787-103">V classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83787-104">文字 V で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="83787-104">System API classes that start with the letter V.</span></span>

<a name="class-validateeventargs"></a><span data-ttu-id="83787-105">クラス ValidateEventArgs</span><span class="sxs-lookup"><span data-stu-id="83787-105">Class ValidateEventArgs</span></span>
-----------------------

    class ValidateEventArgs extends DataEventArgs

### <a name="remarks"></a><span data-ttu-id="83787-106">備考</span><span class="sxs-lookup"><span data-stu-id="83787-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-107">例</span><span class="sxs-lookup"><span data-stu-id="83787-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-108">Methods</span></span>

| <span data-ttu-id="83787-109">方法</span><span class="sxs-lookup"><span data-stu-id="83787-109">Method</span></span>                                                | <span data-ttu-id="83787-110">説明</span><span class="sxs-lookup"><span data-stu-id="83787-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| <span data-ttu-id="83787-111">public boolean parmValidateResult(\[boolean result\])</span><span class="sxs-lookup"><span data-stu-id="83787-111">public boolean parmValidateResult(\[boolean result\])</span></span> |             |
| <span data-ttu-id="83787-112">public void new(boolean result)</span><span class="sxs-lookup"><span data-stu-id="83787-112">public void new(boolean result)</span></span>                       |             |

### <a name="method-parmvalidateresult"></a><span data-ttu-id="83787-113">メソッド parmValidateResult</span><span class="sxs-lookup"><span data-stu-id="83787-113">Method parmValidateResult</span></span>

    public boolean parmValidateResult([boolean result])

#### <a name="parameters"></a><span data-ttu-id="83787-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-114">Parameters</span></span>

<span data-ttu-id="83787-115">件の結果</span><span class="sxs-lookup"><span data-stu-id="83787-115">result</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-116">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="83787-117">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-117">Method new</span></span>

    public void new(boolean result)

#### <a name="parameters"></a><span data-ttu-id="83787-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-118">Parameters</span></span>

<span data-ttu-id="83787-119">件の結果</span><span class="sxs-lookup"><span data-stu-id="83787-119">result</span></span>  

## <a name="class-validatefieldeventargs"></a><span data-ttu-id="83787-120">クラス ValidateFieldEventArgs</span><span class="sxs-lookup"><span data-stu-id="83787-120">Class ValidateFieldEventArgs</span></span>
    class ValidateFieldEventArgs extends ValidateEventArgs

### <a name="remarks"></a><span data-ttu-id="83787-121">備考</span><span class="sxs-lookup"><span data-stu-id="83787-121">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-122">例</span><span class="sxs-lookup"><span data-stu-id="83787-122">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-123">Methods</span></span>

| <span data-ttu-id="83787-124">方法</span><span class="sxs-lookup"><span data-stu-id="83787-124">Method</span></span>                                       | <span data-ttu-id="83787-125">説明</span><span class="sxs-lookup"><span data-stu-id="83787-125">Description</span></span> |
|----------------------------------------------|-------------|
| <span data-ttu-id="83787-126">public int parmFieldId()</span><span class="sxs-lookup"><span data-stu-id="83787-126">public int parmFieldId()</span></span>                     |             |
| <span data-ttu-id="83787-127">public void new(int fieldId, boolean result)</span><span class="sxs-lookup"><span data-stu-id="83787-127">public void new(int fieldId, boolean result)</span></span> |             |

### <a name="method-parmfieldid"></a><span data-ttu-id="83787-128">メソッド parmFieldId</span><span class="sxs-lookup"><span data-stu-id="83787-128">Method parmFieldId</span></span>

    public int parmFieldId()

#### <a name="return-value"></a><span data-ttu-id="83787-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-129">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="83787-130">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-130">Method new</span></span>

    public void new(int fieldId, boolean result)

#### <a name="parameters"></a><span data-ttu-id="83787-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-131">Parameters</span></span>

<span data-ttu-id="83787-132">fieldId</span><span class="sxs-lookup"><span data-stu-id="83787-132">fieldId</span></span>  

<!-- -->

<span data-ttu-id="83787-133">件の結果</span><span class="sxs-lookup"><span data-stu-id="83787-133">result</span></span>  

## <a name="class-validatefieldvalueeventargs"></a><span data-ttu-id="83787-134">クラス ValidateFieldValueEventArgs</span><span class="sxs-lookup"><span data-stu-id="83787-134">Class ValidateFieldValueEventArgs</span></span>
    class ValidateFieldValueEventArgs extends ValidateEventArgs

### <a name="remarks"></a><span data-ttu-id="83787-135">備考</span><span class="sxs-lookup"><span data-stu-id="83787-135">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-136">例</span><span class="sxs-lookup"><span data-stu-id="83787-136">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-137">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-137">Methods</span></span>

| <span data-ttu-id="83787-138">方法</span><span class="sxs-lookup"><span data-stu-id="83787-138">Method</span></span>                                                         | <span data-ttu-id="83787-139">説明</span><span class="sxs-lookup"><span data-stu-id="83787-139">Description</span></span> |
|----------------------------------------------------------------|-------------|
| <span data-ttu-id="83787-140">public str parmFieldName()</span><span class="sxs-lookup"><span data-stu-id="83787-140">public str parmFieldName()</span></span>                                     |             |
| <span data-ttu-id="83787-141">public int parmArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="83787-141">public int parmArrayIndex()</span></span>                                    |             |
| <span data-ttu-id="83787-142">public void new(str fieldName, int arrayIndex, boolean result)</span><span class="sxs-lookup"><span data-stu-id="83787-142">public void new(str fieldName, int arrayIndex, boolean result)</span></span> |             |

### <a name="method-parmfieldname"></a><span data-ttu-id="83787-143">メソッド parmFieldName</span><span class="sxs-lookup"><span data-stu-id="83787-143">Method parmFieldName</span></span>

    public str parmFieldName()

#### <a name="return-value"></a><span data-ttu-id="83787-144">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-144">Return Value</span></span>

### <a name="method-parmarrayindex"></a><span data-ttu-id="83787-145">メソッド parmArrayIndex</span><span class="sxs-lookup"><span data-stu-id="83787-145">Method parmArrayIndex</span></span>

    public int parmArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="83787-146">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-146">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="83787-147">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-147">Method new</span></span>

    public void new(str fieldName, int arrayIndex, boolean result)

#### <a name="parameters"></a><span data-ttu-id="83787-148">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-148">Parameters</span></span>

<span data-ttu-id="83787-149">fieldName</span><span class="sxs-lookup"><span data-stu-id="83787-149">fieldName</span></span>  

<!-- -->

<span data-ttu-id="83787-150">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="83787-150">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="83787-151">件の結果</span><span class="sxs-lookup"><span data-stu-id="83787-151">result</span></span>  

## <a name="class-virtualchannelmanager"></a><span data-ttu-id="83787-152">クラス VirtualChannelManager</span><span class="sxs-lookup"><span data-stu-id="83787-152">Class VirtualChannelManager</span></span>
    class VirtualChannelManager extends Object

### <a name="remarks"></a><span data-ttu-id="83787-153">備考</span><span class="sxs-lookup"><span data-stu-id="83787-153">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-154">例</span><span class="sxs-lookup"><span data-stu-id="83787-154">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-155">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-155">Methods</span></span>

| <span data-ttu-id="83787-156">方法</span><span class="sxs-lookup"><span data-stu-id="83787-156">Method</span></span>                                         | <span data-ttu-id="83787-157">説明</span><span class="sxs-lookup"><span data-stu-id="83787-157">Description</span></span>                                                    |
|------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="83787-158">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="83787-158">public void finalize()</span></span>                         |                                                                |
| <span data-ttu-id="83787-159">public void new()</span><span class="sxs-lookup"><span data-stu-id="83787-159">public void new()</span></span>                              | <span data-ttu-id="83787-160">VirtualChannelManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-160">Initializes a new instance of the VirtualChannelManager class.</span></span> |
| <span data-ttu-id="83787-161">public void sendData(int listenerId, str data)</span><span class="sxs-lookup"><span data-stu-id="83787-161">public void sendData(int listenerId, str data)</span></span> |                                                                |

### <a name="method-finalize"></a><span data-ttu-id="83787-162">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="83787-162">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="83787-163">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-163">Method new</span></span>

<span data-ttu-id="83787-164">VirtualChannelManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-164">Initializes a new instance of the VirtualChannelManager class.</span></span>

    public void new()

### <a name="method-senddata"></a><span data-ttu-id="83787-165">メソッド sendData</span><span class="sxs-lookup"><span data-stu-id="83787-165">Method sendData</span></span>

    public void sendData(int listenerId, str data)

#### <a name="parameters"></a><span data-ttu-id="83787-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-166">Parameters</span></span>

<span data-ttu-id="83787-167">listenerId</span><span class="sxs-lookup"><span data-stu-id="83787-167">listenerId</span></span>  

<!-- -->

<span data-ttu-id="83787-168">データ</span><span class="sxs-lookup"><span data-stu-id="83787-168">data</span></span>  

## <a name="class-vsitemnode"></a><span data-ttu-id="83787-169">クラス VSItemNode</span><span class="sxs-lookup"><span data-stu-id="83787-169">Class VSItemNode</span></span>
    class VSItemNode extends TreeNode

<span data-ttu-id="83787-170">VSItemNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードの基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="83787-170">The VSItemNode class is a base class for Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-171">備考</span><span class="sxs-lookup"><span data-stu-id="83787-171">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-172">例</span><span class="sxs-lookup"><span data-stu-id="83787-172">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-173">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-173">Methods</span></span>

| <span data-ttu-id="83787-174">方法</span><span class="sxs-lookup"><span data-stu-id="83787-174">Method</span></span>                                                             | <span data-ttu-id="83787-175">説明</span><span class="sxs-lookup"><span data-stu-id="83787-175">Description</span></span>                                          |
|--------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83787-176">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="83787-176">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="83787-177">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-177">Returns the source code of this node.</span></span>                |
| <span data-ttu-id="83787-178">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="83787-178">public BinData getFileData()</span></span>                                       |                                                      |
| <span data-ttu-id="83787-179">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="83787-179">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> | <span data-ttu-id="83787-180">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-180">Notifies listeners that a file has been deleted.</span></span>     |
| <span data-ttu-id="83787-181">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-181">::public static void notifyFileUpdated(TreeNode node)</span></span>              | <span data-ttu-id="83787-182">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-182">Notifies listeners that a file has been updated.</span></span>     |
| <span data-ttu-id="83787-183">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="83787-183">public void setFileData(BinData data)</span></span>                              |                                                      |
| <span data-ttu-id="83787-184">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="83787-184">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="83787-185">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-185">Sets the source code of this node.</span></span>                   |
| <span data-ttu-id="83787-186">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-186">public void getFile(str fileName)</span></span>                                  |                                                      |
| <span data-ttu-id="83787-187">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-187">::public static void notifyFileCreated(TreeNode node)</span></span>              | <span data-ttu-id="83787-188">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-188">Notifies listeners that a new file has been created.</span></span> |
| <span data-ttu-id="83787-189">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="83787-189">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> | <span data-ttu-id="83787-190">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-190">Notifies listeners that a file has been renamed.</span></span>     |
| <span data-ttu-id="83787-191">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-191">public void setFile(str fileName)</span></span>                                  |                                                      |

### <a name="method-aotgetsource"></a><span data-ttu-id="83787-192">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="83787-192">Method AOTgetSource</span></span>

<span data-ttu-id="83787-193">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-193">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="83787-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-194">Return Value</span></span>

<span data-ttu-id="83787-195">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="83787-195">The string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-196">備考</span><span class="sxs-lookup"><span data-stu-id="83787-196">Remarks</span></span>

<span data-ttu-id="83787-197">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="83787-197">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="83787-198">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="83787-198">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="83787-199">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-199">Return Value</span></span>

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="83787-200">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="83787-200">Method notifyFileDeleted</span></span>

<span data-ttu-id="83787-201">ファイルが削除されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-201">Notifies listeners that a file has been deleted.</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="83787-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-202">Parameters</span></span>

<span data-ttu-id="83787-203">node</span><span class="sxs-lookup"><span data-stu-id="83787-203">node</span></span>  
<span data-ttu-id="83787-204">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="83787-204">The AOT path of the file.</span></span>

<!-- -->

<span data-ttu-id="83787-205">aotPath</span><span class="sxs-lookup"><span data-stu-id="83787-205">aotPath</span></span>  
<span data-ttu-id="83787-206">ファイルの AOT パス。</span><span class="sxs-lookup"><span data-stu-id="83787-206">The AOT path of the file.</span></span>

### <a name="method-notifyfileupdated"></a><span data-ttu-id="83787-207">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="83787-207">Method notifyFileUpdated</span></span>

<span data-ttu-id="83787-208">ファイルが更新されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-208">Notifies listeners that a file has been updated.</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-209">Parameters</span></span>

<span data-ttu-id="83787-210">node</span><span class="sxs-lookup"><span data-stu-id="83787-210">node</span></span>  
<span data-ttu-id="83787-211">更新ノード。</span><span class="sxs-lookup"><span data-stu-id="83787-211">The node that has been updated.</span></span>

### <a name="method-setfiledata"></a><span data-ttu-id="83787-212">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="83787-212">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="83787-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-213">Parameters</span></span>

<span data-ttu-id="83787-214">データ</span><span class="sxs-lookup"><span data-stu-id="83787-214">data</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="83787-215">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="83787-215">Method AOTsetSource</span></span>

<span data-ttu-id="83787-216">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-216">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="83787-217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-217">Parameters</span></span>

<span data-ttu-id="83787-218">ソース</span><span class="sxs-lookup"><span data-stu-id="83787-218">source</span></span>  
<span data-ttu-id="83787-219">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-219">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="83787-220">isStatic</span><span class="sxs-lookup"><span data-stu-id="83787-220">isStatic</span></span>  
<span data-ttu-id="83787-221">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-221">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-222">備考</span><span class="sxs-lookup"><span data-stu-id="83787-222">Remarks</span></span>

<span data-ttu-id="83787-223">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="83787-223">This method is overridden by nodes that have source code.</span></span>

### <a name="method-getfile"></a><span data-ttu-id="83787-224">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="83787-224">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-225">Parameters</span></span>

<span data-ttu-id="83787-226">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-226">fileName</span></span>  

### <a name="method-notifyfilecreated"></a><span data-ttu-id="83787-227">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="83787-227">Method notifyFileCreated</span></span>

<span data-ttu-id="83787-228">新しいファイルが作成されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-228">Notifies listeners that a new file has been created.</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-229">Parameters</span></span>

<span data-ttu-id="83787-230">node</span><span class="sxs-lookup"><span data-stu-id="83787-230">node</span></span>  
<span data-ttu-id="83787-231">作成されたノード。</span><span class="sxs-lookup"><span data-stu-id="83787-231">The node that has been created.</span></span>

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="83787-232">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="83787-232">Method notifyFileRenamed</span></span>

<span data-ttu-id="83787-233">ファイルの名前が変更されたことをリスナーに通知します。</span><span class="sxs-lookup"><span data-stu-id="83787-233">Notifies listeners that a file has been renamed.</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="83787-234">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-234">Parameters</span></span>

<span data-ttu-id="83787-235">node</span><span class="sxs-lookup"><span data-stu-id="83787-235">node</span></span>  
<span data-ttu-id="83787-236">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="83787-236">The old name of the file.</span></span>

<!-- -->

<span data-ttu-id="83787-237">oldName</span><span class="sxs-lookup"><span data-stu-id="83787-237">oldName</span></span>  
<span data-ttu-id="83787-238">ファイルの古い名前。</span><span class="sxs-lookup"><span data-stu-id="83787-238">The old name of the file.</span></span>

### <a name="method-setfile"></a><span data-ttu-id="83787-239">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="83787-239">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-240">Parameters</span></span>

<span data-ttu-id="83787-241">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-241">fileName</span></span>  

## <a name="class-vsprojectfilenode"></a><span data-ttu-id="83787-242">クラス VSProjectFileNode</span><span class="sxs-lookup"><span data-stu-id="83787-242">Class VSProjectFileNode</span></span>
    class VSProjectFileNode extends VSItemNode

<span data-ttu-id="83787-243">VSProjectFileNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでファイルを表します。</span><span class="sxs-lookup"><span data-stu-id="83787-243">The VSProjectFileNode class represents files in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-244">備考</span><span class="sxs-lookup"><span data-stu-id="83787-244">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-245">例</span><span class="sxs-lookup"><span data-stu-id="83787-245">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-246">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-246">Methods</span></span>

| <span data-ttu-id="83787-247">方法</span><span class="sxs-lookup"><span data-stu-id="83787-247">Method</span></span>                                                             | <span data-ttu-id="83787-248">説明</span><span class="sxs-lookup"><span data-stu-id="83787-248">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="83787-249">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="83787-249">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="83787-250">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-250">Returns the source code of this node.</span></span> |
| <span data-ttu-id="83787-251">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="83787-251">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="83787-252">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-252">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="83787-253">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="83787-253">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="83787-254">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-254">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="83787-255">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="83787-255">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |
| <span data-ttu-id="83787-256">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-256">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="83787-257">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-257">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="83787-258">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="83787-258">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="83787-259">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="83787-259">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="83787-260">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-260">Sets the source code of this node.</span></span>    |

### <a name="method-aotgetsource"></a><span data-ttu-id="83787-261">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="83787-261">Method AOTgetSource</span></span>

<span data-ttu-id="83787-262">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-262">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="83787-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-263">Return Value</span></span>

<span data-ttu-id="83787-264">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="83787-264">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-265">備考</span><span class="sxs-lookup"><span data-stu-id="83787-265">Remarks</span></span>

<span data-ttu-id="83787-266">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="83787-266">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="83787-267">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="83787-267">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="83787-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-268">Return Value</span></span>

### <a name="method-notifyfilecreated"></a><span data-ttu-id="83787-269">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="83787-269">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-270">Parameters</span></span>

<span data-ttu-id="83787-271">node</span><span class="sxs-lookup"><span data-stu-id="83787-271">node</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="83787-272">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="83787-272">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="83787-273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-273">Parameters</span></span>

<span data-ttu-id="83787-274">データ</span><span class="sxs-lookup"><span data-stu-id="83787-274">data</span></span>  

### <a name="method-getfile"></a><span data-ttu-id="83787-275">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="83787-275">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-276">Parameters</span></span>

<span data-ttu-id="83787-277">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-277">fileName</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="83787-278">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="83787-278">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="83787-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-279">Parameters</span></span>

<span data-ttu-id="83787-280">node</span><span class="sxs-lookup"><span data-stu-id="83787-280">node</span></span>  

<!-- -->

<span data-ttu-id="83787-281">aotPath</span><span class="sxs-lookup"><span data-stu-id="83787-281">aotPath</span></span>  

### <a name="method-notifyfileupdated"></a><span data-ttu-id="83787-282">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="83787-282">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-283">Parameters</span></span>

<span data-ttu-id="83787-284">node</span><span class="sxs-lookup"><span data-stu-id="83787-284">node</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="83787-285">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="83787-285">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-286">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-286">Parameters</span></span>

<span data-ttu-id="83787-287">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-287">fileName</span></span>  

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="83787-288">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="83787-288">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="83787-289">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-289">Parameters</span></span>

<span data-ttu-id="83787-290">node</span><span class="sxs-lookup"><span data-stu-id="83787-290">node</span></span>  

<!-- -->

<span data-ttu-id="83787-291">oldName</span><span class="sxs-lookup"><span data-stu-id="83787-291">oldName</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="83787-292">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="83787-292">Method AOTsetSource</span></span>

<span data-ttu-id="83787-293">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-293">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="83787-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-294">Parameters</span></span>

<span data-ttu-id="83787-295">ソース</span><span class="sxs-lookup"><span data-stu-id="83787-295">source</span></span>  
<span data-ttu-id="83787-296">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-296">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="83787-297">isStatic</span><span class="sxs-lookup"><span data-stu-id="83787-297">isStatic</span></span>  
<span data-ttu-id="83787-298">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-298">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-299">備考</span><span class="sxs-lookup"><span data-stu-id="83787-299">Remarks</span></span>

<span data-ttu-id="83787-300">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="83787-300">This method is overridden by nodes that have source code.</span></span>

## <a name="class-vsprojectfoldernode"></a><span data-ttu-id="83787-301">クラス VSProjectFolderNode</span><span class="sxs-lookup"><span data-stu-id="83787-301">Class VSProjectFolderNode</span></span>
    class VSProjectFolderNode extends TreeNode

<span data-ttu-id="83787-302">VSProjectFolderNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="83787-302">The VSProjectFolderNode class represents folders in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-303">備考</span><span class="sxs-lookup"><span data-stu-id="83787-303">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-304">例</span><span class="sxs-lookup"><span data-stu-id="83787-304">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-305">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-305">Methods</span></span>

| <span data-ttu-id="83787-306">方法</span><span class="sxs-lookup"><span data-stu-id="83787-306">Method</span></span>                                                                                       | <span data-ttu-id="83787-307">説明</span><span class="sxs-lookup"><span data-stu-id="83787-307">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83787-308">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="83787-308">public str AOTgetSource()</span></span>                                                                    | <span data-ttu-id="83787-309">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-309">Returns the source code of this node.</span></span>                                                                    |
| <span data-ttu-id="83787-310">public VSProjectFileNode createFileNode(str name)</span><span class="sxs-lookup"><span data-stu-id="83787-310">public VSProjectFileNode createFileNode(str name)</span></span>                                            | <span data-ttu-id="83787-311">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-311">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="83787-312">public VSProjectFolderNode createFolderNode(str name)</span><span class="sxs-lookup"><span data-stu-id="83787-312">public VSProjectFolderNode createFolderNode(str name)</span></span>                                        | <span data-ttu-id="83787-313">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-313">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span> |
| <span data-ttu-id="83787-314">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span><span class="sxs-lookup"><span data-stu-id="83787-314">public VSProjectLinkNode createLinkNode(str name, str aotPath, \[boolean createLinkedNode\])</span></span> | <span data-ttu-id="83787-315">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-315">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>   |
| <span data-ttu-id="83787-316">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="83787-316">public BinData getFileData()</span></span>                                                                 |                                                                                                          |
| <span data-ttu-id="83787-317">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-317">::public static void notifyFileUpdated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="83787-318">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="83787-318">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span>                           |                                                                                                          |
| <span data-ttu-id="83787-319">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="83787-319">public void setFileData(BinData data)</span></span>                                                        |                                                                                                          |
| <span data-ttu-id="83787-320">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="83787-320">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>                                   | <span data-ttu-id="83787-321">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-321">Sets the source code of this node.</span></span>                                                                       |
| <span data-ttu-id="83787-322">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-322">public void getFile(str fileName)</span></span>                                                            |                                                                                                          |
| <span data-ttu-id="83787-323">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-323">::public static void notifyFileCreated(TreeNode node)</span></span>                                        |                                                                                                          |
| <span data-ttu-id="83787-324">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="83787-324">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span>                           |                                                                                                          |
| <span data-ttu-id="83787-325">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-325">public void setFile(str fileName)</span></span>                                                            |                                                                                                          |

### <a name="method-aotgetsource"></a><span data-ttu-id="83787-326">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="83787-326">Method AOTgetSource</span></span>

<span data-ttu-id="83787-327">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-327">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="83787-328">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-328">Return Value</span></span>

<span data-ttu-id="83787-329">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="83787-329">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-330">備考</span><span class="sxs-lookup"><span data-stu-id="83787-330">Remarks</span></span>

<span data-ttu-id="83787-331">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="83787-331">This function is overridden by nodes that have source code.</span></span>

### <a name="method-createfilenode"></a><span data-ttu-id="83787-332">メソッド createFileNode</span><span class="sxs-lookup"><span data-stu-id="83787-332">Method createFileNode</span></span>

<span data-ttu-id="83787-333">この VSProjectFolderNode インスタンスの子として、VSProjectFileNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-333">Creates a new instance of the VSProjectFileNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectFileNode createFileNode(str name)

#### <a name="parameters"></a><span data-ttu-id="83787-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-334">Parameters</span></span>

<span data-ttu-id="83787-335">名前</span><span class="sxs-lookup"><span data-stu-id="83787-335">name</span></span>  
<span data-ttu-id="83787-336">ファイル ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="83787-336">The name of the file node.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-337">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-337">Return Value</span></span>

<span data-ttu-id="83787-338">VSProjectFileNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="83787-338">The new instance of the VSProjectFileNode class.</span></span>

### <a name="method-createfoldernode"></a><span data-ttu-id="83787-339">メソッド createFolderNode</span><span class="sxs-lookup"><span data-stu-id="83787-339">Method createFolderNode</span></span>

<span data-ttu-id="83787-340">この VSProjectFolderNode インスタンスの子として、VSProjectFolderNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-340">Creates a new instance of the VSProjectFolderNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectFolderNode createFolderNode(str name)

#### <a name="parameters"></a><span data-ttu-id="83787-341">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-341">Parameters</span></span>

<span data-ttu-id="83787-342">名前</span><span class="sxs-lookup"><span data-stu-id="83787-342">name</span></span>  
<span data-ttu-id="83787-343">フォルダー ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="83787-343">The name of the folder node.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-344">Return Value</span></span>

<span data-ttu-id="83787-345">VSProjectFolderNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="83787-345">The new instance of the VSProjectFolderNode class.</span></span>

### <a name="method-createlinknode"></a><span data-ttu-id="83787-346">メソッド createLinkNode</span><span class="sxs-lookup"><span data-stu-id="83787-346">Method createLinkNode</span></span>

<span data-ttu-id="83787-347">この VSProjectFolderNode インスタンスの子として、VSProjectLinkNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-347">Creates a new instance of the VSProjectLinkNode class as a child of this VSProjectFolderNode instance.</span></span>

    public VSProjectLinkNode createLinkNode(str name, str aotPath, [boolean createLinkedNode])

#### <a name="parameters"></a><span data-ttu-id="83787-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-348">Parameters</span></span>

<span data-ttu-id="83787-349">名前</span><span class="sxs-lookup"><span data-stu-id="83787-349">name</span></span>  

<!-- -->

<span data-ttu-id="83787-350">aotPath</span><span class="sxs-lookup"><span data-stu-id="83787-350">aotPath</span></span>  

<!-- -->

<span data-ttu-id="83787-351">createLinkedNode</span><span class="sxs-lookup"><span data-stu-id="83787-351">createLinkedNode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-352">Return Value</span></span>

<span data-ttu-id="83787-353">VSProjectLinkNode クラスの新しいインスタンス。</span><span class="sxs-lookup"><span data-stu-id="83787-353">The new instance of the VSProjectLinkNode class.</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="83787-354">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="83787-354">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="83787-355">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-355">Return Value</span></span>

### <a name="method-notifyfileupdated"></a><span data-ttu-id="83787-356">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="83787-356">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-357">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-357">Parameters</span></span>

<span data-ttu-id="83787-358">node</span><span class="sxs-lookup"><span data-stu-id="83787-358">node</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="83787-359">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="83787-359">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="83787-360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-360">Parameters</span></span>

<span data-ttu-id="83787-361">node</span><span class="sxs-lookup"><span data-stu-id="83787-361">node</span></span>  

<!-- -->

<span data-ttu-id="83787-362">aotPath</span><span class="sxs-lookup"><span data-stu-id="83787-362">aotPath</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="83787-363">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="83787-363">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="83787-364">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-364">Parameters</span></span>

<span data-ttu-id="83787-365">データ</span><span class="sxs-lookup"><span data-stu-id="83787-365">data</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="83787-366">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="83787-366">Method AOTsetSource</span></span>

<span data-ttu-id="83787-367">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-367">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="83787-368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-368">Parameters</span></span>

<span data-ttu-id="83787-369">ソース</span><span class="sxs-lookup"><span data-stu-id="83787-369">source</span></span>  
<span data-ttu-id="83787-370">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-370">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="83787-371">isStatic</span><span class="sxs-lookup"><span data-stu-id="83787-371">isStatic</span></span>  
<span data-ttu-id="83787-372">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-372">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-373">備考</span><span class="sxs-lookup"><span data-stu-id="83787-373">Remarks</span></span>

<span data-ttu-id="83787-374">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="83787-374">This method is overridden by nodes that have source code.</span></span>

### <a name="method-getfile"></a><span data-ttu-id="83787-375">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="83787-375">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-376">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-376">Parameters</span></span>

<span data-ttu-id="83787-377">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-377">fileName</span></span>  

### <a name="method-notifyfilecreated"></a><span data-ttu-id="83787-378">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="83787-378">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-379">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-379">Parameters</span></span>

<span data-ttu-id="83787-380">node</span><span class="sxs-lookup"><span data-stu-id="83787-380">node</span></span>  

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="83787-381">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="83787-381">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="83787-382">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-382">Parameters</span></span>

<span data-ttu-id="83787-383">node</span><span class="sxs-lookup"><span data-stu-id="83787-383">node</span></span>  

<!-- -->

<span data-ttu-id="83787-384">oldName</span><span class="sxs-lookup"><span data-stu-id="83787-384">oldName</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="83787-385">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="83787-385">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-386">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-386">Parameters</span></span>

<span data-ttu-id="83787-387">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-387">fileName</span></span>  

## <a name="class-vsprojectlinknode"></a><span data-ttu-id="83787-388">クラス VSProjectLinkNode</span><span class="sxs-lookup"><span data-stu-id="83787-388">Class VSProjectLinkNode</span></span>
    class VSProjectLinkNode extends VSItemNode

<span data-ttu-id="83787-389">VSProjectLinkNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードにある別の Finance and Operations AOT へのリンクを表します。</span><span class="sxs-lookup"><span data-stu-id="83787-389">The VSProjectLinkNode class represents links to other Finance and Operations Application Object Tree (AOT) nodes in the Microsoft Visual Studio project nodes in the AOT.</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-390">備考</span><span class="sxs-lookup"><span data-stu-id="83787-390">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-391">例</span><span class="sxs-lookup"><span data-stu-id="83787-391">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-392">方法</span><span class="sxs-lookup"><span data-stu-id="83787-392">Methods</span></span>

| <span data-ttu-id="83787-393">方法</span><span class="sxs-lookup"><span data-stu-id="83787-393">Method</span></span>                                                             | <span data-ttu-id="83787-394">説明</span><span class="sxs-lookup"><span data-stu-id="83787-394">Description</span></span>                           |
|--------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="83787-395">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="83787-395">public str AOTgetSource()</span></span>                                          | <span data-ttu-id="83787-396">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-396">Returns the source code of this node.</span></span> |
| <span data-ttu-id="83787-397">public str getAOTPath()</span><span class="sxs-lookup"><span data-stu-id="83787-397">public str getAOTPath()</span></span>                                            |                                       |
| <span data-ttu-id="83787-398">public BinData getFileData()</span><span class="sxs-lookup"><span data-stu-id="83787-398">public BinData getFileData()</span></span>                                       |                                       |
| <span data-ttu-id="83787-399">::public static void notifyFileCreated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-399">::public static void notifyFileCreated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="83787-400">public void setFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-400">public void setFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="83787-401">public void setFileData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="83787-401">public void setFileData(BinData data)</span></span>                              |                                       |
| <span data-ttu-id="83787-402">public void getFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="83787-402">public void getFile(str fileName)</span></span>                                  |                                       |
| <span data-ttu-id="83787-403">::public static void notifyFileUpdated(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="83787-403">::public static void notifyFileUpdated(TreeNode node)</span></span>              |                                       |
| <span data-ttu-id="83787-404">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="83787-404">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>         | <span data-ttu-id="83787-405">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-405">Sets the source code of this node.</span></span>    |
| <span data-ttu-id="83787-406">::public static void notifyFileRenamed(TreeNode node, str oldName)</span><span class="sxs-lookup"><span data-stu-id="83787-406">::public static void notifyFileRenamed(TreeNode node, str oldName)</span></span> |                                       |
| <span data-ttu-id="83787-407">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span><span class="sxs-lookup"><span data-stu-id="83787-407">::public static void notifyFileDeleted(TreeNode node, str aotPath)</span></span> |                                       |

### <a name="method-aotgetsource"></a><span data-ttu-id="83787-408">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="83787-408">Method AOTgetSource</span></span>

<span data-ttu-id="83787-409">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="83787-409">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="83787-410">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-410">Return Value</span></span>

<span data-ttu-id="83787-411">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="83787-411">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-412">備考</span><span class="sxs-lookup"><span data-stu-id="83787-412">Remarks</span></span>

<span data-ttu-id="83787-413">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="83787-413">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getaotpath"></a><span data-ttu-id="83787-414">メソッド getAOTPath</span><span class="sxs-lookup"><span data-stu-id="83787-414">Method getAOTPath</span></span>

    public str getAOTPath()

#### <a name="return-value"></a><span data-ttu-id="83787-415">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-415">Return Value</span></span>

### <a name="method-getfiledata"></a><span data-ttu-id="83787-416">メソッド getFileData</span><span class="sxs-lookup"><span data-stu-id="83787-416">Method getFileData</span></span>

    public BinData getFileData()

#### <a name="return-value"></a><span data-ttu-id="83787-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-417">Return Value</span></span>

### <a name="method-notifyfilecreated"></a><span data-ttu-id="83787-418">メソッド notifyFileCreated</span><span class="sxs-lookup"><span data-stu-id="83787-418">Method notifyFileCreated</span></span>

    public static void notifyFileCreated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-419">Parameters</span></span>

<span data-ttu-id="83787-420">node</span><span class="sxs-lookup"><span data-stu-id="83787-420">node</span></span>  

### <a name="method-setfile"></a><span data-ttu-id="83787-421">メソッド setFile</span><span class="sxs-lookup"><span data-stu-id="83787-421">Method setFile</span></span>

    public void setFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-422">Parameters</span></span>

<span data-ttu-id="83787-423">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-423">fileName</span></span>  

### <a name="method-setfiledata"></a><span data-ttu-id="83787-424">メソッド setFileData</span><span class="sxs-lookup"><span data-stu-id="83787-424">Method setFileData</span></span>

    public void setFileData(BinData data)

#### <a name="parameters"></a><span data-ttu-id="83787-425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-425">Parameters</span></span>

<span data-ttu-id="83787-426">データ</span><span class="sxs-lookup"><span data-stu-id="83787-426">data</span></span>  

### <a name="method-getfile"></a><span data-ttu-id="83787-427">メソッド getFile</span><span class="sxs-lookup"><span data-stu-id="83787-427">Method getFile</span></span>

    public void getFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="83787-428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-428">Parameters</span></span>

<span data-ttu-id="83787-429">fileName</span><span class="sxs-lookup"><span data-stu-id="83787-429">fileName</span></span>  

### <a name="method-notifyfileupdated"></a><span data-ttu-id="83787-430">メソッド notifyFileUpdated</span><span class="sxs-lookup"><span data-stu-id="83787-430">Method notifyFileUpdated</span></span>

    public static void notifyFileUpdated(TreeNode node)

#### <a name="parameters"></a><span data-ttu-id="83787-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-431">Parameters</span></span>

<span data-ttu-id="83787-432">node</span><span class="sxs-lookup"><span data-stu-id="83787-432">node</span></span>  

### <a name="method-aotsetsource"></a><span data-ttu-id="83787-433">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="83787-433">Method AOTsetSource</span></span>

<span data-ttu-id="83787-434">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-434">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="83787-435">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-435">Parameters</span></span>

<span data-ttu-id="83787-436">ソース</span><span class="sxs-lookup"><span data-stu-id="83787-436">source</span></span>  
<span data-ttu-id="83787-437">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-437">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="83787-438">isStatic</span><span class="sxs-lookup"><span data-stu-id="83787-438">isStatic</span></span>  
<span data-ttu-id="83787-439">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="83787-439">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-440">備考</span><span class="sxs-lookup"><span data-stu-id="83787-440">Remarks</span></span>

<span data-ttu-id="83787-441">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="83787-441">This method is overridden by nodes that have source code.</span></span>

### <a name="method-notifyfilerenamed"></a><span data-ttu-id="83787-442">メソッド notifyFileRenamed</span><span class="sxs-lookup"><span data-stu-id="83787-442">Method notifyFileRenamed</span></span>

    public static void notifyFileRenamed(TreeNode node, str oldName)

#### <a name="parameters"></a><span data-ttu-id="83787-443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-443">Parameters</span></span>

<span data-ttu-id="83787-444">node</span><span class="sxs-lookup"><span data-stu-id="83787-444">node</span></span>  

<!-- -->

<span data-ttu-id="83787-445">oldName</span><span class="sxs-lookup"><span data-stu-id="83787-445">oldName</span></span>  

### <a name="method-notifyfiledeleted"></a><span data-ttu-id="83787-446">メソッド notifyFileDeleted</span><span class="sxs-lookup"><span data-stu-id="83787-446">Method notifyFileDeleted</span></span>

    public static void notifyFileDeleted(TreeNode node, str aotPath)

#### <a name="parameters"></a><span data-ttu-id="83787-447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-447">Parameters</span></span>

<span data-ttu-id="83787-448">node</span><span class="sxs-lookup"><span data-stu-id="83787-448">node</span></span>  

<!-- -->

<span data-ttu-id="83787-449">aotPath</span><span class="sxs-lookup"><span data-stu-id="83787-449">aotPath</span></span>  

## <a name="class-vsprojectnode"></a><span data-ttu-id="83787-450">クラス VSProjectNode</span><span class="sxs-lookup"><span data-stu-id="83787-450">Class VSProjectNode</span></span>
    class VSProjectNode extends xResourceNode

<span data-ttu-id="83787-451">VSProjectNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでプロジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="83787-451">The VSProjectNode class represents projects in the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-452">備考</span><span class="sxs-lookup"><span data-stu-id="83787-452">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-453">例</span><span class="sxs-lookup"><span data-stu-id="83787-453">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-454">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-454">Methods</span></span>

| <span data-ttu-id="83787-455">方法</span><span class="sxs-lookup"><span data-stu-id="83787-455">Method</span></span>                                                                | <span data-ttu-id="83787-456">説明</span><span class="sxs-lookup"><span data-stu-id="83787-456">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83787-457">public container extract(\[str path\], \[boolean extractReferenced\])</span><span class="sxs-lookup"><span data-stu-id="83787-457">public container extract(\[str path\], \[boolean extractReferenced\])</span></span> | <span data-ttu-id="83787-458">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="83787-458">Extracts the whole project to disk.</span></span>                                                               |
| <span data-ttu-id="83787-459">public VSProjectFolderNode getContentNode()</span><span class="sxs-lookup"><span data-stu-id="83787-459">public VSProjectFolderNode getContentNode()</span></span>                           | <span data-ttu-id="83787-460">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-460">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>        |
| <span data-ttu-id="83787-461">public DeployTo getDeployTo()</span><span class="sxs-lookup"><span data-stu-id="83787-461">public DeployTo getDeployTo()</span></span>                                         | <span data-ttu-id="83787-462">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-462">Gets value of the deployTo property.</span></span>                                                              |
| <span data-ttu-id="83787-463">public VSProjectFolderNode getOutputNode()</span><span class="sxs-lookup"><span data-stu-id="83787-463">public VSProjectFolderNode getOutputNode()</span></span>                            | <span data-ttu-id="83787-464">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-464">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>  |
| <span data-ttu-id="83787-465">public VSProjectFileNode getPrimaryOutputNode()</span><span class="sxs-lookup"><span data-stu-id="83787-465">public VSProjectFileNode getPrimaryOutputNode()</span></span>                       | <span data-ttu-id="83787-466">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-466">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span> |
| <span data-ttu-id="83787-467">public str getPrimaryTargetFileName()</span><span class="sxs-lookup"><span data-stu-id="83787-467">public str getPrimaryTargetFileName()</span></span>                                 | <span data-ttu-id="83787-468">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-468">Gets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="83787-469">public Map getProxies()</span><span class="sxs-lookup"><span data-stu-id="83787-469">public Map getProxies()</span></span>                                               | <span data-ttu-id="83787-470">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-470">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="83787-471">public container getProxiesContainer()</span><span class="sxs-lookup"><span data-stu-id="83787-471">public container getProxiesContainer()</span></span>                                | <span data-ttu-id="83787-472">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-472">Gets the proxies in this project.</span></span>                                                                 |
| <span data-ttu-id="83787-473">public str getReferencedProjectsInAOT()</span><span class="sxs-lookup"><span data-stu-id="83787-473">public str getReferencedProjectsInAOT()</span></span>                               | <span data-ttu-id="83787-474">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-474">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>             |
| <span data-ttu-id="83787-475">public str referencedProjects(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="83787-475">public str referencedProjects(\[str value\])</span></span>                          |                                                                                                   |
| <span data-ttu-id="83787-476">public void setPrimaryTargetFileName(str targetFileName)</span><span class="sxs-lookup"><span data-stu-id="83787-476">public void setPrimaryTargetFileName(str targetFileName)</span></span>              | <span data-ttu-id="83787-477">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-477">Sets the primary target file name of the Visual Studio project.</span></span>                                   |
| <span data-ttu-id="83787-478">public void extractToSpecificDir(str directory)</span><span class="sxs-lookup"><span data-stu-id="83787-478">public void extractToSpecificDir(str directory)</span></span>                       |                                                                                                   |
| <span data-ttu-id="83787-479">public void setDeployTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="83787-479">public void setDeployTo(DeployTo deployTo)</span></span>                            | <span data-ttu-id="83787-480">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-480">Sets the value of the deployTo property.</span></span>                                                          |

### <a name="method-extract"></a><span data-ttu-id="83787-481">メソッド extract</span><span class="sxs-lookup"><span data-stu-id="83787-481">Method extract</span></span>

<span data-ttu-id="83787-482">ディスクにプロジェクト全体を展開します。</span><span class="sxs-lookup"><span data-stu-id="83787-482">Extracts the whole project to disk.</span></span>

    public container extract([str path], [boolean extractReferenced])

#### <a name="parameters"></a><span data-ttu-id="83787-483">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-483">Parameters</span></span>

<span data-ttu-id="83787-484">path</span><span class="sxs-lookup"><span data-stu-id="83787-484">path</span></span>  
<span data-ttu-id="83787-485">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="83787-485">A Boolean value that determines whether to extract the referenced projects.</span></span>

<!-- -->

<span data-ttu-id="83787-486">extractReferenced</span><span class="sxs-lookup"><span data-stu-id="83787-486">extractReferenced</span></span>  
<span data-ttu-id="83787-487">参照されるプロジェクトを抽出するかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="83787-487">A Boolean value that determines whether to extract the referenced projects.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-488">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-488">Return Value</span></span>

<span data-ttu-id="83787-489">プロジェクトの展開先のパスの一覧。</span><span class="sxs-lookup"><span data-stu-id="83787-489">A list of paths where the project was extracted.</span></span>

### <a name="method-getcontentnode"></a><span data-ttu-id="83787-490">メソッド getContentNode</span><span class="sxs-lookup"><span data-stu-id="83787-490">Method getContentNode</span></span>

<span data-ttu-id="83787-491">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-491">Gets the content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

    public VSProjectFolderNode getContentNode()

#### <a name="return-value"></a><span data-ttu-id="83787-492">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-492">Return Value</span></span>

<span data-ttu-id="83787-493">Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83787-493">The content VSProjectFolderNode object that contains the Visual Studio project files.</span></span>

### <a name="method-getdeployto"></a><span data-ttu-id="83787-494">メソッド getDeployTo</span><span class="sxs-lookup"><span data-stu-id="83787-494">Method getDeployTo</span></span>

<span data-ttu-id="83787-495">deployTo プロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-495">Gets value of the deployTo property.</span></span>

    public DeployTo getDeployTo()

#### <a name="return-value"></a><span data-ttu-id="83787-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-496">Return Value</span></span>

<span data-ttu-id="83787-497">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="83787-497">The deployTo property value.</span></span>

### <a name="method-getoutputnode"></a><span data-ttu-id="83787-498">メソッド getOutputNode</span><span class="sxs-lookup"><span data-stu-id="83787-498">Method getOutputNode</span></span>

<span data-ttu-id="83787-499">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-499">Gets the output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

    public VSProjectFolderNode getOutputNode()

#### <a name="return-value"></a><span data-ttu-id="83787-500">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-500">Return Value</span></span>

<span data-ttu-id="83787-501">Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83787-501">The output VSProjectFolderNode object that contains the Visual Studio project output files.</span></span>

### <a name="method-getprimaryoutputnode"></a><span data-ttu-id="83787-502">メソッド getPrimaryOutputNode</span><span class="sxs-lookup"><span data-stu-id="83787-502">Method getPrimaryOutputNode</span></span>

<span data-ttu-id="83787-503">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-503">Gets the VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

    public VSProjectFileNode getPrimaryOutputNode()

#### <a name="return-value"></a><span data-ttu-id="83787-504">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-504">Return Value</span></span>

<span data-ttu-id="83787-505">Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83787-505">A VSProjectFileNode object that represent the primary output of the Visual Studio project.</span></span>

### <a name="method-getprimarytargetfilename"></a><span data-ttu-id="83787-506">メソッド getPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="83787-506">Method getPrimaryTargetFileName</span></span>

<span data-ttu-id="83787-507">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-507">Gets the primary target file name of the Visual Studio project.</span></span>

    public str getPrimaryTargetFileName()

#### <a name="return-value"></a><span data-ttu-id="83787-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-508">Return Value</span></span>

<span data-ttu-id="83787-509">Visual Studio プロジェクトのプライマリ ターゲット ファイル名。</span><span class="sxs-lookup"><span data-stu-id="83787-509">The primary target file name of the Visual Studio project.</span></span>

### <a name="method-getproxies"></a><span data-ttu-id="83787-510">メソッド getProxies</span><span class="sxs-lookup"><span data-stu-id="83787-510">Method getProxies</span></span>

<span data-ttu-id="83787-511">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-511">Gets the proxies in this project.</span></span>

    public Map getProxies()

#### <a name="return-value"></a><span data-ttu-id="83787-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-512">Return Value</span></span>

<span data-ttu-id="83787-513">クラス、列挙、およびテーブルのキーを含むマップ。</span><span class="sxs-lookup"><span data-stu-id="83787-513">A map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="83787-514">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="83787-514">Each key contains a list of proxies.</span></span>

### <a name="method-getproxiescontainer"></a><span data-ttu-id="83787-515">メソッド getProxiesContainer</span><span class="sxs-lookup"><span data-stu-id="83787-515">Method getProxiesContainer</span></span>

<span data-ttu-id="83787-516">このプロジェクトでのプロキシを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-516">Gets the proxies in this project.</span></span>

    public container getProxiesContainer()

#### <a name="return-value"></a><span data-ttu-id="83787-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-517">Return Value</span></span>

<span data-ttu-id="83787-518">マップの梱包済み表現を保持するコンテナーには、Class、Enum、Table のキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="83787-518">A container that holds the packed representation of a map that contains the Class, Enum, and Table keys.</span></span> <span data-ttu-id="83787-519">各キーには、プロキシのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="83787-519">Each key contains a list of proxies.</span></span>

### <a name="method-getreferencedprojectsinaot"></a><span data-ttu-id="83787-520">メソッド getReferencedProjectsInAOT</span><span class="sxs-lookup"><span data-stu-id="83787-520">Method getReferencedProjectsInAOT</span></span>

<span data-ttu-id="83787-521">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-521">Gets the AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

    public str getReferencedProjectsInAOT()

#### <a name="return-value"></a><span data-ttu-id="83787-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-522">Return Value</span></span>

<span data-ttu-id="83787-523">この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスの一覧。</span><span class="sxs-lookup"><span data-stu-id="83787-523">A list of AOT paths of the projects that are referenced by this Visual Studio project.</span></span>

### <a name="method-referencedprojects"></a><span data-ttu-id="83787-524">メソッド referencedProjects</span><span class="sxs-lookup"><span data-stu-id="83787-524">Method referencedProjects</span></span>

    public str referencedProjects([str value])

#### <a name="parameters"></a><span data-ttu-id="83787-525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-525">Parameters</span></span>

<span data-ttu-id="83787-526">値</span><span class="sxs-lookup"><span data-stu-id="83787-526">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-527">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-527">Return Value</span></span>

### <a name="method-setprimarytargetfilename"></a><span data-ttu-id="83787-528">メソッド setPrimaryTargetFileName</span><span class="sxs-lookup"><span data-stu-id="83787-528">Method setPrimaryTargetFileName</span></span>

<span data-ttu-id="83787-529">Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-529">Sets the primary target file name of the Visual Studio project.</span></span>

    public void setPrimaryTargetFileName(str targetFileName)

#### <a name="parameters"></a><span data-ttu-id="83787-530">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-530">Parameters</span></span>

<span data-ttu-id="83787-531">targetFileName</span><span class="sxs-lookup"><span data-stu-id="83787-531">targetFileName</span></span>  
<span data-ttu-id="83787-532">Visual Studio プロジェクトのプライマリ ターゲット ファイル名。</span><span class="sxs-lookup"><span data-stu-id="83787-532">The primary target file name of the Visual Studio project.</span></span>

### <a name="method-extracttospecificdir"></a><span data-ttu-id="83787-533">メソッド extractToSpecificDir</span><span class="sxs-lookup"><span data-stu-id="83787-533">Method extractToSpecificDir</span></span>

    public void extractToSpecificDir(str directory)

#### <a name="parameters"></a><span data-ttu-id="83787-534">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-534">Parameters</span></span>

<span data-ttu-id="83787-535">directory</span><span class="sxs-lookup"><span data-stu-id="83787-535">directory</span></span>  

### <a name="method-setdeployto"></a><span data-ttu-id="83787-536">メソッド setDeployTo</span><span class="sxs-lookup"><span data-stu-id="83787-536">Method setDeployTo</span></span>

<span data-ttu-id="83787-537">deployTo プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="83787-537">Sets the value of the deployTo property.</span></span>

    public void setDeployTo(DeployTo deployTo)

#### <a name="parameters"></a><span data-ttu-id="83787-538">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-538">Parameters</span></span>

<span data-ttu-id="83787-539">deployTo</span><span class="sxs-lookup"><span data-stu-id="83787-539">deployTo</span></span>  
<span data-ttu-id="83787-540">deployTo プロパティ値。</span><span class="sxs-lookup"><span data-stu-id="83787-540">The deployTo property value.</span></span>

## <a name="class-vsprojectsnode"></a><span data-ttu-id="83787-541">クラス VSProjectsNode</span><span class="sxs-lookup"><span data-stu-id="83787-541">Class VSProjectsNode</span></span>
    class VSProjectsNode extends xResourceNode

<span data-ttu-id="83787-542">VSProjectNode クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードのルートです。</span><span class="sxs-lookup"><span data-stu-id="83787-542">The VSProjectNode class is the root of the Microsoft Visual Studio project nodes in the Finance and Operations Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-543">備考</span><span class="sxs-lookup"><span data-stu-id="83787-543">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-544">例</span><span class="sxs-lookup"><span data-stu-id="83787-544">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-545">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-545">Methods</span></span>

| <span data-ttu-id="83787-546">方法</span><span class="sxs-lookup"><span data-stu-id="83787-546">Method</span></span>                                                                                            | <span data-ttu-id="83787-547">説明</span><span class="sxs-lookup"><span data-stu-id="83787-547">Description</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="83787-548">public TreeNode AOTfindChild(str name, \[int nodeType\])</span><span class="sxs-lookup"><span data-stu-id="83787-548">public TreeNode AOTfindChild(str name, \[int nodeType\])</span></span>                                          | <span data-ttu-id="83787-549">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="83787-549">Finds the specified child node of this node.</span></span>                                               |
| <span data-ttu-id="83787-550">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span><span class="sxs-lookup"><span data-stu-id="83787-550">public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\])</span></span> | <span data-ttu-id="83787-551">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-551">Creates a new instance of the VSProjectNode class.</span></span>                                         |
| <span data-ttu-id="83787-552">public container getProjectsDeployingTo(DeployTo deployTo)</span><span class="sxs-lookup"><span data-stu-id="83787-552">public container getProjectsDeployingTo(DeployTo deployTo)</span></span>                                        | <span data-ttu-id="83787-553">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-553">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>            |
| <span data-ttu-id="83787-554">public container getProjectsModifiedAfter(DateTime timestamp)</span><span class="sxs-lookup"><span data-stu-id="83787-554">public container getProjectsModifiedAfter(DateTime timestamp)</span></span>                                     | <span data-ttu-id="83787-555">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-555">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span> |
| <span data-ttu-id="83787-556">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span><span class="sxs-lookup"><span data-stu-id="83787-556">public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)</span></span>                              |                                                                                            |
| <span data-ttu-id="83787-557">public Object getVSProjectNodeObservable()</span><span class="sxs-lookup"><span data-stu-id="83787-557">public Object getVSProjectNodeObservable()</span></span>                                                        | <span data-ttu-id="83787-558">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-558">Gets the VSProjectNodeObservable object.</span></span>                                                   |
| <span data-ttu-id="83787-559">public void AOTrefresh()</span><span class="sxs-lookup"><span data-stu-id="83787-559">public void AOTrefresh()</span></span>                                                                          | <span data-ttu-id="83787-560">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="83787-560">Updates the node with the latest changes to the .aod file.</span></span>                                 |

### <a name="method-aotfindchild"></a><span data-ttu-id="83787-561">メソッド AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="83787-561">Method AOTfindChild</span></span>

<span data-ttu-id="83787-562">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="83787-562">Finds the specified child node of this node.</span></span>

    public TreeNode AOTfindChild(str name, [int nodeType])

#### <a name="parameters"></a><span data-ttu-id="83787-563">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-563">Parameters</span></span>

<span data-ttu-id="83787-564">名前</span><span class="sxs-lookup"><span data-stu-id="83787-564">name</span></span>  

<!-- -->

<span data-ttu-id="83787-565">nodeType</span><span class="sxs-lookup"><span data-stu-id="83787-565">nodeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-566">Return Value</span></span>

<span data-ttu-id="83787-567">指定したツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="83787-567">The specified tree node.</span></span>

### <a name="method-createprojectnode"></a><span data-ttu-id="83787-568">メソッド createProjectNode</span><span class="sxs-lookup"><span data-stu-id="83787-568">Method createProjectNode</span></span>

<span data-ttu-id="83787-569">VSProjectNode クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="83787-569">Creates a new instance of the VSProjectNode class.</span></span>

    public VSProjectNode createProjectNode(str name, str projectTypesString, [boolean virtualNode])

#### <a name="parameters"></a><span data-ttu-id="83787-570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-570">Parameters</span></span>

<span data-ttu-id="83787-571">名前</span><span class="sxs-lookup"><span data-stu-id="83787-571">name</span></span>  
<span data-ttu-id="83787-572">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="83787-572">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="83787-573">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="83787-573">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="83787-574">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="83787-574">projectTypesString</span></span>  
<span data-ttu-id="83787-575">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="83787-575">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="83787-576">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="83787-576">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

<!-- -->

<span data-ttu-id="83787-577">virtualNode</span><span class="sxs-lookup"><span data-stu-id="83787-577">virtualNode</span></span>  
<span data-ttu-id="83787-578">ノードがメモリ内でのみ作成されるかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="83787-578">A Boolean value that indicates whether the node is created only in memory.</span></span> <span data-ttu-id="83787-579">この場合、ノードは Finance and Operations ストアで保持されません。</span><span class="sxs-lookup"><span data-stu-id="83787-579">In this case, the node will not be persisted in the Finance and Operations Store.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-580">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-580">Return Value</span></span>

<span data-ttu-id="83787-581">作成された VSProjectNode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83787-581">The VSProjectNode object that is created.</span></span>

### <a name="method-getprojectsdeployingto"></a><span data-ttu-id="83787-582">メソッド getProjectsDeployingTo</span><span class="sxs-lookup"><span data-stu-id="83787-582">Method getProjectsDeployingTo</span></span>

<span data-ttu-id="83787-583">指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-583">Gets a list of VSProjectNode objects that have the specified deployTo property.</span></span>

    public container getProjectsDeployingTo(DeployTo deployTo)

#### <a name="parameters"></a><span data-ttu-id="83787-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-584">Parameters</span></span>

<span data-ttu-id="83787-585">deployTo</span><span class="sxs-lookup"><span data-stu-id="83787-585">deployTo</span></span>  
<span data-ttu-id="83787-586">deployTo プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="83787-586">The value of the deployTo property.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-587">Return Value</span></span>

<span data-ttu-id="83787-588">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="83787-588">A list of VSProjectNode objects.</span></span>

### <a name="method-getprojectsmodifiedafter"></a><span data-ttu-id="83787-589">メソッド getProjectsModifiedAfter</span><span class="sxs-lookup"><span data-stu-id="83787-589">Method getProjectsModifiedAfter</span></span>

<span data-ttu-id="83787-590">指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-590">Gets a list of VSProjectNode objects that were modified after the specified date and time.</span></span>

    public container getProjectsModifiedAfter(DateTime timestamp)

#### <a name="parameters"></a><span data-ttu-id="83787-591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-591">Parameters</span></span>

<span data-ttu-id="83787-592">timestamp</span><span class="sxs-lookup"><span data-stu-id="83787-592">timestamp</span></span>  
<span data-ttu-id="83787-593">DB\_DATETIME\_TYPE 値としての日時。</span><span class="sxs-lookup"><span data-stu-id="83787-593">The date and time as a DB\_DATETIME\_TYPE value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="83787-594">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-594">Return Value</span></span>

<span data-ttu-id="83787-595">VSProjectNode オブジェクトの一覧。</span><span class="sxs-lookup"><span data-stu-id="83787-595">A list of VSProjectNode objects.</span></span>

### <a name="method-gettypenodefromguid"></a><span data-ttu-id="83787-596">メソッド getTypeNodeFromGuid</span><span class="sxs-lookup"><span data-stu-id="83787-596">Method getTypeNodeFromGuid</span></span>

    public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)

#### <a name="parameters"></a><span data-ttu-id="83787-597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-597">Parameters</span></span>

<span data-ttu-id="83787-598">projectTypesString</span><span class="sxs-lookup"><span data-stu-id="83787-598">projectTypesString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-599">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-599">Return Value</span></span>

### <a name="method-getvsprojectnodeobservable"></a><span data-ttu-id="83787-600">メソッド getVSProjectNodeObservable</span><span class="sxs-lookup"><span data-stu-id="83787-600">Method getVSProjectNodeObservable</span></span>

<span data-ttu-id="83787-601">VSProjectNodeObservable オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="83787-601">Gets the VSProjectNodeObservable object.</span></span>

    public Object getVSProjectNodeObservable()

#### <a name="return-value"></a><span data-ttu-id="83787-602">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-602">Return Value</span></span>

<span data-ttu-id="83787-603">VSProjectNodeObservable オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83787-603">The VSProjectNodeObservable object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="83787-604">備考</span><span class="sxs-lookup"><span data-stu-id="83787-604">Remarks</span></span>

<span data-ttu-id="83787-605">オブザーバーはこれで登録でき、Visual Studio プロジェクトで CRUD 操作の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="83787-605">Observers can register with this and get notified of CRUD operations on Visual Studio projects.</span></span>

### <a name="method-aotrefresh"></a><span data-ttu-id="83787-606">メソッド AOTrefresh</span><span class="sxs-lookup"><span data-stu-id="83787-606">Method AOTrefresh</span></span>

<span data-ttu-id="83787-607">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="83787-607">Updates the node with the latest changes to the .aod file.</span></span>

    public void AOTrefresh()

## <a name="class-vsprojecttypenode"></a><span data-ttu-id="83787-608">クラス VSProjectTypeNode</span><span class="sxs-lookup"><span data-stu-id="83787-608">Class VSProjectTypeNode</span></span>
    class VSProjectTypeNode extends TreeNode

<span data-ttu-id="83787-609">VSProjectTypeNode クラスは、AOT 内の Visual Studio プロジェクト ノードでプロジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="83787-609">The VSProjectTypeNode class represents project types in the Visual Studio Project nodes in the AOT.</span></span>

### <a name="remarks"></a><span data-ttu-id="83787-610">備考</span><span class="sxs-lookup"><span data-stu-id="83787-610">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-611">例</span><span class="sxs-lookup"><span data-stu-id="83787-611">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-612">方法</span><span class="sxs-lookup"><span data-stu-id="83787-612">Methods</span></span>

| <span data-ttu-id="83787-613">方法</span><span class="sxs-lookup"><span data-stu-id="83787-613">Method</span></span> | <span data-ttu-id="83787-614">説明</span><span class="sxs-lookup"><span data-stu-id="83787-614">Description</span></span> |
|--------|-------------|
|        |             |

## <a name="class-vss"></a><span data-ttu-id="83787-615">クラス VSS</span><span class="sxs-lookup"><span data-stu-id="83787-615">Class VSS</span></span>
    class VSS extends Object

### <a name="remarks"></a><span data-ttu-id="83787-616">備考</span><span class="sxs-lookup"><span data-stu-id="83787-616">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-617">例</span><span class="sxs-lookup"><span data-stu-id="83787-617">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-618">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-618">Methods</span></span>

| <span data-ttu-id="83787-619">方法</span><span class="sxs-lookup"><span data-stu-id="83787-619">Method</span></span>                                                                                                        | <span data-ttu-id="83787-620">説明</span><span class="sxs-lookup"><span data-stu-id="83787-620">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="83787-621">public boolean connect()</span><span class="sxs-lookup"><span data-stu-id="83787-621">public boolean connect()</span></span>                                                                                      |                                           |
| <span data-ttu-id="83787-622">public boolean connected()</span><span class="sxs-lookup"><span data-stu-id="83787-622">public boolean connected()</span></span>                                                                                    |                                           |
| <span data-ttu-id="83787-623">public boolean disconnect()</span><span class="sxs-lookup"><span data-stu-id="83787-623">public boolean disconnect()</span></span>                                                                                   |                                           |
| <span data-ttu-id="83787-624">public container getCheckedoutFiles()</span><span class="sxs-lookup"><span data-stu-id="83787-624">public container getCheckedoutFiles()</span></span>                                                                         |                                           |
| <span data-ttu-id="83787-625">public container getConnectionInfo()</span><span class="sxs-lookup"><span data-stu-id="83787-625">public container getConnectionInfo()</span></span>                                                                          |                                           |
| <span data-ttu-id="83787-626">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span><span class="sxs-lookup"><span data-stu-id="83787-626">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span></span>      |                                           |
| <span data-ttu-id="83787-627">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span><span class="sxs-lookup"><span data-stu-id="83787-627">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span></span>                |                                           |
| <span data-ttu-id="83787-628">public VSSItem newSubProject(str name, str localPath)</span><span class="sxs-lookup"><span data-stu-id="83787-628">public VSSItem newSubProject(str name, str localPath)</span></span>                                                         |                                           |
| <span data-ttu-id="83787-629">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span><span class="sxs-lookup"><span data-stu-id="83787-629">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span></span> |                                           |
| <span data-ttu-id="83787-630">public void new()</span><span class="sxs-lookup"><span data-stu-id="83787-630">public void new()</span></span>                                                                                             | <span data-ttu-id="83787-631">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-631">Initializes an instance of the VSS class.</span></span> |

### <a name="method-connect"></a><span data-ttu-id="83787-632">メソッド connect</span><span class="sxs-lookup"><span data-stu-id="83787-632">Method connect</span></span>

    public boolean connect()

#### <a name="return-value"></a><span data-ttu-id="83787-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-633">Return Value</span></span>

### <a name="method-connected"></a><span data-ttu-id="83787-634">メソッド connected</span><span class="sxs-lookup"><span data-stu-id="83787-634">Method connected</span></span>

    public boolean connected()

#### <a name="return-value"></a><span data-ttu-id="83787-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-635">Return Value</span></span>

### <a name="method-disconnect"></a><span data-ttu-id="83787-636">メソッド disconnect</span><span class="sxs-lookup"><span data-stu-id="83787-636">Method disconnect</span></span>

    public boolean disconnect()

#### <a name="return-value"></a><span data-ttu-id="83787-637">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-637">Return Value</span></span>

### <a name="method-getcheckedoutfiles"></a><span data-ttu-id="83787-638">メソッド getCheckedoutFiles</span><span class="sxs-lookup"><span data-stu-id="83787-638">Method getCheckedoutFiles</span></span>

    public container getCheckedoutFiles()

#### <a name="return-value"></a><span data-ttu-id="83787-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-639">Return Value</span></span>

### <a name="method-getconnectioninfo"></a><span data-ttu-id="83787-640">メソッド getConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="83787-640">Method getConnectionInfo</span></span>

    public container getConnectionInfo()

#### <a name="return-value"></a><span data-ttu-id="83787-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-641">Return Value</span></span>

### <a name="method-getvssitem"></a><span data-ttu-id="83787-642">メソッド getVSSItem</span><span class="sxs-lookup"><span data-stu-id="83787-642">Method getVSSItem</span></span>

    public VSSItem getVSSItem(str vssItemPath, str localFilePath, [boolean completePath], [int version])

#### <a name="parameters"></a><span data-ttu-id="83787-643">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-643">Parameters</span></span>

<span data-ttu-id="83787-644">vssItemPath</span><span class="sxs-lookup"><span data-stu-id="83787-644">vssItemPath</span></span>  

<!-- -->

<span data-ttu-id="83787-645">localFilePath</span><span class="sxs-lookup"><span data-stu-id="83787-645">localFilePath</span></span>  

<!-- -->

<span data-ttu-id="83787-646">completePath</span><span class="sxs-lookup"><span data-stu-id="83787-646">completePath</span></span>  

<!-- -->

<span data-ttu-id="83787-647">のバージョン</span><span class="sxs-lookup"><span data-stu-id="83787-647">version</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-648">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-648">Return Value</span></span>

### <a name="method-init"></a><span data-ttu-id="83787-649">メソッド init</span><span class="sxs-lookup"><span data-stu-id="83787-649">Method init</span></span>

    public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)

#### <a name="parameters"></a><span data-ttu-id="83787-650">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-650">Parameters</span></span>

<span data-ttu-id="83787-651">vssIni</span><span class="sxs-lookup"><span data-stu-id="83787-651">vssIni</span></span>  

<!-- -->

<span data-ttu-id="83787-652">vssPrjRoot</span><span class="sxs-lookup"><span data-stu-id="83787-652">vssPrjRoot</span></span>  

<!-- -->

<span data-ttu-id="83787-653">vssWorkingFolder</span><span class="sxs-lookup"><span data-stu-id="83787-653">vssWorkingFolder</span></span>  

<!-- -->

<span data-ttu-id="83787-654">vssUser</span><span class="sxs-lookup"><span data-stu-id="83787-654">vssUser</span></span>  

<!-- -->

<span data-ttu-id="83787-655">vssPwd</span><span class="sxs-lookup"><span data-stu-id="83787-655">vssPwd</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-656">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-656">Return Value</span></span>

### <a name="method-newsubproject"></a><span data-ttu-id="83787-657">メソッド newSubProject</span><span class="sxs-lookup"><span data-stu-id="83787-657">Method newSubProject</span></span>

    public VSSItem newSubProject(str name, str localPath)

#### <a name="parameters"></a><span data-ttu-id="83787-658">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-658">Parameters</span></span>

<span data-ttu-id="83787-659">名前</span><span class="sxs-lookup"><span data-stu-id="83787-659">name</span></span>  

<!-- -->

<span data-ttu-id="83787-660">localPath</span><span class="sxs-lookup"><span data-stu-id="83787-660">localPath</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-661">Return Value</span></span>

### <a name="method-synchronizeprojects"></a><span data-ttu-id="83787-662">メソッド synchronizeProjects</span><span class="sxs-lookup"><span data-stu-id="83787-662">Method synchronizeProjects</span></span>

    public Map synchronizeProjects([Set projects], [boolean force], [boolean delLocalFiles], [str label])

#### <a name="parameters"></a><span data-ttu-id="83787-663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-663">Parameters</span></span>

<span data-ttu-id="83787-664">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="83787-664">projects</span></span>  

<!-- -->

<span data-ttu-id="83787-665">force</span><span class="sxs-lookup"><span data-stu-id="83787-665">force</span></span>  

<!-- -->

<span data-ttu-id="83787-666">delLocalFiles</span><span class="sxs-lookup"><span data-stu-id="83787-666">delLocalFiles</span></span>  

<!-- -->

<span data-ttu-id="83787-667">ラベル</span><span class="sxs-lookup"><span data-stu-id="83787-667">label</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-668">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-668">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="83787-669">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-669">Method new</span></span>

<span data-ttu-id="83787-670">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-670">Initializes an instance of the VSS class.</span></span>

    public void new()

## <a name="class-vssitem"></a><span data-ttu-id="83787-671">クラス VSSItem</span><span class="sxs-lookup"><span data-stu-id="83787-671">Class VSSItem</span></span>
    class VSSItem extends Object

### <a name="remarks"></a><span data-ttu-id="83787-672">備考</span><span class="sxs-lookup"><span data-stu-id="83787-672">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="83787-673">例</span><span class="sxs-lookup"><span data-stu-id="83787-673">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="83787-674">メソッド</span><span class="sxs-lookup"><span data-stu-id="83787-674">Methods</span></span>

| <span data-ttu-id="83787-675">方法</span><span class="sxs-lookup"><span data-stu-id="83787-675">Method</span></span>                                                                               | <span data-ttu-id="83787-676">説明</span><span class="sxs-lookup"><span data-stu-id="83787-676">Description</span></span>                                      |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="83787-677">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="83787-677">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span></span>                      |                                                  |
| <span data-ttu-id="83787-678">public boolean checkin(\[str comment\])</span><span class="sxs-lookup"><span data-stu-id="83787-678">public boolean checkin(\[str comment\])</span></span>                                              |                                                  |
| <span data-ttu-id="83787-679">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span><span class="sxs-lookup"><span data-stu-id="83787-679">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span></span> |                                                  |
| <span data-ttu-id="83787-680">public boolean delete()</span><span class="sxs-lookup"><span data-stu-id="83787-680">public boolean delete()</span></span>                                                              |                                                  |
| <span data-ttu-id="83787-681">public boolean destroy()</span><span class="sxs-lookup"><span data-stu-id="83787-681">public boolean destroy()</span></span>                                                             |                                                  |
| <span data-ttu-id="83787-682">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span><span class="sxs-lookup"><span data-stu-id="83787-682">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span></span> |                                                  |
| <span data-ttu-id="83787-683">public str getActionText()</span><span class="sxs-lookup"><span data-stu-id="83787-683">public str getActionText()</span></span>                                                           |                                                  |
| <span data-ttu-id="83787-684">public container getCheckedOutTo()</span><span class="sxs-lookup"><span data-stu-id="83787-684">public container getCheckedOutTo()</span></span>                                                   |                                                  |
| <span data-ttu-id="83787-685">public int getCheckoutVersion()</span><span class="sxs-lookup"><span data-stu-id="83787-685">public int getCheckoutVersion()</span></span>                                                      |                                                  |
| <span data-ttu-id="83787-686">public container getHistory()</span><span class="sxs-lookup"><span data-stu-id="83787-686">public container getHistory()</span></span>                                                        |                                                  |
| <span data-ttu-id="83787-687">public ComInterface getIUnknown()</span><span class="sxs-lookup"><span data-stu-id="83787-687">public ComInterface getIUnknown()</span></span>                                                    |                                                  |
| <span data-ttu-id="83787-688">public int getVersionNo()</span><span class="sxs-lookup"><span data-stu-id="83787-688">public int getVersionNo()</span></span>                                                            |                                                  |
| <span data-ttu-id="83787-689">public str getVSSPath()</span><span class="sxs-lookup"><span data-stu-id="83787-689">public str getVSSPath()</span></span>                                                              |                                                  |
| <span data-ttu-id="83787-690">public boolean isCheckedOut()</span><span class="sxs-lookup"><span data-stu-id="83787-690">public boolean isCheckedOut()</span></span>                                                        |                                                  |
| <span data-ttu-id="83787-691">public boolean isRenamed()</span><span class="sxs-lookup"><span data-stu-id="83787-691">public boolean isRenamed()</span></span>                                                           |                                                  |
| <span data-ttu-id="83787-692">public str name(str newName)</span><span class="sxs-lookup"><span data-stu-id="83787-692">public str name(str newName)</span></span>                                                         |                                                  |
| <span data-ttu-id="83787-693">public boolean rename(str newName)</span><span class="sxs-lookup"><span data-stu-id="83787-693">public boolean rename(str newName)</span></span>                                                   |                                                  |
| <span data-ttu-id="83787-694">public boolean undoCheckout()</span><span class="sxs-lookup"><span data-stu-id="83787-694">public boolean undoCheckout()</span></span>                                                        |                                                  |
| <span data-ttu-id="83787-695">private void new()</span><span class="sxs-lookup"><span data-stu-id="83787-695">private void new()</span></span>                                                                   | <span data-ttu-id="83787-696">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-696">Initializes a new instance of the VSSItem class.</span></span> |

### <a name="method-add"></a><span data-ttu-id="83787-697">メソッド add</span><span class="sxs-lookup"><span data-stu-id="83787-697">Method add</span></span>

    public boolean add([boolean keepCheckedout], [str comment])

#### <a name="parameters"></a><span data-ttu-id="83787-698">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-698">Parameters</span></span>

<span data-ttu-id="83787-699">keepCheckedout</span><span class="sxs-lookup"><span data-stu-id="83787-699">keepCheckedout</span></span>  

<!-- -->

<span data-ttu-id="83787-700">comment</span><span class="sxs-lookup"><span data-stu-id="83787-700">comment</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-701">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-701">Return Value</span></span>

### <a name="method-checkin"></a><span data-ttu-id="83787-702">メソッド checkin</span><span class="sxs-lookup"><span data-stu-id="83787-702">Method checkin</span></span>

    public boolean checkin([str comment])

#### <a name="parameters"></a><span data-ttu-id="83787-703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-703">Parameters</span></span>

<span data-ttu-id="83787-704">comment</span><span class="sxs-lookup"><span data-stu-id="83787-704">comment</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-705">Return Value</span></span>

### <a name="method-checkout"></a><span data-ttu-id="83787-706">メソッド checkout</span><span class="sxs-lookup"><span data-stu-id="83787-706">Method checkout</span></span>

    public boolean checkout([boolean allowMultipleCheckout], [boolean replaceLocal])

#### <a name="parameters"></a><span data-ttu-id="83787-707">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-707">Parameters</span></span>

<span data-ttu-id="83787-708">allowMultipleCheckout</span><span class="sxs-lookup"><span data-stu-id="83787-708">allowMultipleCheckout</span></span>  

<!-- -->

<span data-ttu-id="83787-709">replaceLocal</span><span class="sxs-lookup"><span data-stu-id="83787-709">replaceLocal</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-710">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-710">Return Value</span></span>

### <a name="method-delete"></a><span data-ttu-id="83787-711">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="83787-711">Method delete</span></span>

    public boolean delete()

#### <a name="return-value"></a><span data-ttu-id="83787-712">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-712">Return Value</span></span>

### <a name="method-destroy"></a><span data-ttu-id="83787-713">メソッド destroy</span><span class="sxs-lookup"><span data-stu-id="83787-713">Method destroy</span></span>

    public boolean destroy()

#### <a name="return-value"></a><span data-ttu-id="83787-714">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-714">Return Value</span></span>

### <a name="method-get"></a><span data-ttu-id="83787-715">メソッド get</span><span class="sxs-lookup"><span data-stu-id="83787-715">Method get</span></span>

    public Map get([boolean force], [int version], [str label], [str localFile])

#### <a name="parameters"></a><span data-ttu-id="83787-716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-716">Parameters</span></span>

<span data-ttu-id="83787-717">force</span><span class="sxs-lookup"><span data-stu-id="83787-717">force</span></span>  

<!-- -->

<span data-ttu-id="83787-718">のバージョン</span><span class="sxs-lookup"><span data-stu-id="83787-718">version</span></span>  

<!-- -->

<span data-ttu-id="83787-719">ラベル</span><span class="sxs-lookup"><span data-stu-id="83787-719">label</span></span>  

<!-- -->

<span data-ttu-id="83787-720">localFile</span><span class="sxs-lookup"><span data-stu-id="83787-720">localFile</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-721">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-721">Return Value</span></span>

### <a name="method-getactiontext"></a><span data-ttu-id="83787-722">メソッド getActionText</span><span class="sxs-lookup"><span data-stu-id="83787-722">Method getActionText</span></span>

    public str getActionText()

#### <a name="return-value"></a><span data-ttu-id="83787-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-723">Return Value</span></span>

### <a name="method-getcheckedoutto"></a><span data-ttu-id="83787-724">メソッド getCheckedOutTo</span><span class="sxs-lookup"><span data-stu-id="83787-724">Method getCheckedOutTo</span></span>

    public container getCheckedOutTo()

#### <a name="return-value"></a><span data-ttu-id="83787-725">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-725">Return Value</span></span>

### <a name="method-getcheckoutversion"></a><span data-ttu-id="83787-726">メソッド getCheckoutVersion</span><span class="sxs-lookup"><span data-stu-id="83787-726">Method getCheckoutVersion</span></span>

    public int getCheckoutVersion()

#### <a name="return-value"></a><span data-ttu-id="83787-727">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-727">Return Value</span></span>

### <a name="method-gethistory"></a><span data-ttu-id="83787-728">メソッド getHistory</span><span class="sxs-lookup"><span data-stu-id="83787-728">Method getHistory</span></span>

    public container getHistory()

#### <a name="return-value"></a><span data-ttu-id="83787-729">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-729">Return Value</span></span>

### <a name="method-getiunknown"></a><span data-ttu-id="83787-730">メソッド getIUnknown</span><span class="sxs-lookup"><span data-stu-id="83787-730">Method getIUnknown</span></span>

    public ComInterface getIUnknown()

#### <a name="return-value"></a><span data-ttu-id="83787-731">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-731">Return Value</span></span>

### <a name="method-getversionno"></a><span data-ttu-id="83787-732">メソッド getVersionNo</span><span class="sxs-lookup"><span data-stu-id="83787-732">Method getVersionNo</span></span>

    public int getVersionNo()

#### <a name="return-value"></a><span data-ttu-id="83787-733">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-733">Return Value</span></span>

### <a name="method-getvsspath"></a><span data-ttu-id="83787-734">メソッド getVSSPath</span><span class="sxs-lookup"><span data-stu-id="83787-734">Method getVSSPath</span></span>

    public str getVSSPath()

#### <a name="return-value"></a><span data-ttu-id="83787-735">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-735">Return Value</span></span>

### <a name="method-ischeckedout"></a><span data-ttu-id="83787-736">メソッド isCheckedOut</span><span class="sxs-lookup"><span data-stu-id="83787-736">Method isCheckedOut</span></span>

    public boolean isCheckedOut()

#### <a name="return-value"></a><span data-ttu-id="83787-737">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-737">Return Value</span></span>

### <a name="method-isrenamed"></a><span data-ttu-id="83787-738">メソッド isRenamed</span><span class="sxs-lookup"><span data-stu-id="83787-738">Method isRenamed</span></span>

    public boolean isRenamed()

#### <a name="return-value"></a><span data-ttu-id="83787-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-739">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="83787-740">メソッド名</span><span class="sxs-lookup"><span data-stu-id="83787-740">Method name</span></span>

    public str name(str newName)

#### <a name="parameters"></a><span data-ttu-id="83787-741">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-741">Parameters</span></span>

<span data-ttu-id="83787-742">newName</span><span class="sxs-lookup"><span data-stu-id="83787-742">newName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-743">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-743">Return Value</span></span>

### <a name="method-rename"></a><span data-ttu-id="83787-744">メソッド rename</span><span class="sxs-lookup"><span data-stu-id="83787-744">Method rename</span></span>

    public boolean rename(str newName)

#### <a name="parameters"></a><span data-ttu-id="83787-745">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83787-745">Parameters</span></span>

<span data-ttu-id="83787-746">newName</span><span class="sxs-lookup"><span data-stu-id="83787-746">newName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="83787-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-747">Return Value</span></span>

### <a name="method-undocheckout"></a><span data-ttu-id="83787-748">メソッド undoCheckout</span><span class="sxs-lookup"><span data-stu-id="83787-748">Method undoCheckout</span></span>

    public boolean undoCheckout()

#### <a name="return-value"></a><span data-ttu-id="83787-749">戻り値</span><span class="sxs-lookup"><span data-stu-id="83787-749">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="83787-750">メソッド new</span><span class="sxs-lookup"><span data-stu-id="83787-750">Method new</span></span>

<span data-ttu-id="83787-751">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="83787-751">Initializes a new instance of the VSSItem class.</span></span>

    private void new()



