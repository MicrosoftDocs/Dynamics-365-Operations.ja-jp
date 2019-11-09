---
title: L クラス
description: 文字 L で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52291
ms.assetid: 60d8c71b-6df4-4776-9642-ed89ab5ad46a
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d0ea9f496e8375cf57782749e4dbb5c8ae8c9bd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191613"
---
# <a name="l-classes"></a><span data-ttu-id="63d8c-103">L クラス</span><span class="sxs-lookup"><span data-stu-id="63d8c-103">L classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63d8c-104">文字 L で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="63d8c-104">System API classes that start with the letter L.</span></span>

<a name="class-label"></a><span data-ttu-id="63d8c-105">クラス ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-105">Class Label</span></span>
-----------

    class Label extends Object

<span data-ttu-id="63d8c-106">Label クラスは、ラベル ID およびラベル ファイルを管理します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-106">The Label class manages label IDs and label files.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-107">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-107">Remarks</span></span>

<span data-ttu-id="63d8c-108">SysLabel クラスは、Label クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-108">The SysLabel class extends the Label class.</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-109">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-110">Methods</span></span>

| <span data-ttu-id="63d8c-111">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-111">Method</span></span>                                                                | <span data-ttu-id="63d8c-112">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-112">Description</span></span>                                                                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-113">public LabelBulkEditor bulkEditor(str module)</span><span class="sxs-lookup"><span data-stu-id="63d8c-113">public LabelBulkEditor bulkEditor(str module)</span></span>                         | <span data-ttu-id="63d8c-114">LabelBulkEditor クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-114">Creates an instance of the LabelBulkEditor class.</span></span>                                                   |
| <span data-ttu-id="63d8c-115">public boolean createLabelFile(str module, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-115">public boolean createLabelFile(str module, str language)</span></span>              | <span data-ttu-id="63d8c-116">指定されたラベル ID のラベル ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-116">Creates a label file for a specified label ID.</span></span>                                                      |
| <span data-ttu-id="63d8c-117">public boolean delete(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-117">public boolean delete(str label)</span></span>                                      | <span data-ttu-id="63d8c-118">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-118">Deletes a specified label.</span></span>                                                                          |
| <span data-ttu-id="63d8c-119">public boolean exists(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-119">public boolean exists(str label)</span></span>                                      | <span data-ttu-id="63d8c-120">指定したラベル ID が存在するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-120">Indicates whether a specified label ID exists.</span></span>                                                      |
| <span data-ttu-id="63d8c-121">public str extractComment(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-121">public str extractComment(str label)</span></span>                                  | <span data-ttu-id="63d8c-122">指定されたラベル ID に関連付けられているコメントを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-122">Returns a comment that is associated with a specified label ID.</span></span>                                     |
| <span data-ttu-id="63d8c-123">public str extractString(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-123">public str extractString(str label)</span></span>                                   | <span data-ttu-id="63d8c-124">指定されたラベル ID に関連付けられているテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-124">Returns the text that is associated with a specified label ID.</span></span>                                      |
| <span data-ttu-id="63d8c-125">public str getFirstLabelFile()</span><span class="sxs-lookup"><span data-stu-id="63d8c-125">public str getFirstLabelFile()</span></span>                                        | <span data-ttu-id="63d8c-126">最初のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-126">Returns the first label file ID record.</span></span>                                                             |
| <span data-ttu-id="63d8c-127">public Date getLabelFileCreatedDate(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-127">public Date getLabelFileCreatedDate(str labelFile, str language)</span></span>      | <span data-ttu-id="63d8c-128">指定したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-128">Returns the date that a specified label file was created.</span></span>                                           |
| <span data-ttu-id="63d8c-129">public int getLabelFileCreatedTime(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-129">public int getLabelFileCreatedTime(str labelFile, str language)</span></span>       | <span data-ttu-id="63d8c-130">指定したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-130">Returns the time that a specified label file was created.</span></span>                                           |
| <span data-ttu-id="63d8c-131">public Date getLabelFileModificationDate(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-131">public Date getLabelFileModificationDate(str labelFile, str language)</span></span> | <span data-ttu-id="63d8c-132">変更したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-132">Returns the date that a specified label file was modified.</span></span>                                          |
| <span data-ttu-id="63d8c-133">public int getLabelFileModificationTime(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-133">public int getLabelFileModificationTime(str labelFile, str language)</span></span>  | <span data-ttu-id="63d8c-134">変更したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-134">Returns the time that a specified label file was modified.</span></span>                                          |
| <span data-ttu-id="63d8c-135">public str getNextLabelFile()</span><span class="sxs-lookup"><span data-stu-id="63d8c-135">public str getNextLabelFile()</span></span>                                         | <span data-ttu-id="63d8c-136">次のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-136">Returns the next label file ID record.</span></span>                                                              |
| <span data-ttu-id="63d8c-137">public str insert(str text, str comment, str module)</span><span class="sxs-lookup"><span data-stu-id="63d8c-137">public str insert(str text, str comment, str module)</span></span>                  | <span data-ttu-id="63d8c-138">指定されたテキスト文字列のラベル ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-138">Creates a label ID for a specified text string.</span></span>                                                     |
| <span data-ttu-id="63d8c-139">public int labelId(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-139">public int labelId(str label)</span></span>                                         | <span data-ttu-id="63d8c-140">指定したラベル ID に含まれる番号を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-140">Returns the number that is included in a specified label ID.</span></span>                                        |
| <span data-ttu-id="63d8c-141">public int maxLabelId(str module)</span><span class="sxs-lookup"><span data-stu-id="63d8c-141">public int maxLabelId(str module)</span></span>                                     | <span data-ttu-id="63d8c-142">指定したラベル ファイル内の最後のラベルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-142">Returns the ID for the last label in the specified label file.</span></span>                                      |
| <span data-ttu-id="63d8c-143">public boolean modify(str label, str text, \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-143">public boolean modify(str label, str text, \[str comment\])</span></span>           | <span data-ttu-id="63d8c-144">指定されたラベルに関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-144">Modifies the text and comment that are associated with a specified label.</span></span>                           |
| <span data-ttu-id="63d8c-145">public str moduleId(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-145">public str moduleId(str label)</span></span>                                        | <span data-ttu-id="63d8c-146">指定したラベル ID のラベル ファイルを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-146">Returns the label file ID for a specified label ID.</span></span>                                                 |
| <span data-ttu-id="63d8c-147">public boolean moreLabelFiles()</span><span class="sxs-lookup"><span data-stu-id="63d8c-147">public boolean moreLabelFiles()</span></span>                                       | <span data-ttu-id="63d8c-148">追加のラベル ファイルがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-148">Indicates whether there are additional label files.</span></span>                                                 |
| <span data-ttu-id="63d8c-149">public str name(str module, int labelId)</span><span class="sxs-lookup"><span data-stu-id="63d8c-149">public str name(str module, int labelId)</span></span>                              | <span data-ttu-id="63d8c-150">指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-150">Returns a label ID, based on a specified label file ID and label ID number.</span></span>                         |
| <span data-ttu-id="63d8c-151">public str searchFirst(str searchString)</span><span class="sxs-lookup"><span data-stu-id="63d8c-151">public str searchFirst(str searchString)</span></span>                              | <span data-ttu-id="63d8c-152">指定した検索用語で検出された最初のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-152">Returns the first label ID that is found for a specified search term.</span></span>                               |
| <span data-ttu-id="63d8c-153">public str searchNext()</span><span class="sxs-lookup"><span data-stu-id="63d8c-153">public str searchNext()</span></span>                                               | <span data-ttu-id="63d8c-154">searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-154">Returns the next label ID that is found for a search term that is passed to the searchFirst method.</span></span> |
| <span data-ttu-id="63d8c-155">::public static boolean flush(str labelFileId, str language)</span><span class="sxs-lookup"><span data-stu-id="63d8c-155">::public static boolean flush(str labelFileId, str language)</span></span>          | <span data-ttu-id="63d8c-156">ディスクにラベル ファイル バッファーをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-156">Flushes the label file buffers to disk.</span></span>                                                             |
| <span data-ttu-id="63d8c-157">public void new(\[str language\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-157">public void new(\[str language\])</span></span>                                     | <span data-ttu-id="63d8c-158">ラベル クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-158">Creates a new instance of the Label class.</span></span>                                                          |
| <span data-ttu-id="63d8c-159">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="63d8c-159">public void finalize()</span></span>                                                | <span data-ttu-id="63d8c-160">現在のラベル ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-160">Closes the current label file.</span></span>                                                                      |

### <a name="method-bulkeditor"></a><span data-ttu-id="63d8c-161">メソッド bulkEditor</span><span class="sxs-lookup"><span data-stu-id="63d8c-161">Method bulkEditor</span></span>

<span data-ttu-id="63d8c-162">LabelBulkEditor クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-162">Creates an instance of the LabelBulkEditor class.</span></span>

    public LabelBulkEditor bulkEditor(str module)

#### <a name="parameters"></a><span data-ttu-id="63d8c-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-163">Parameters</span></span>

<span data-ttu-id="63d8c-164">モジュール</span><span class="sxs-lookup"><span data-stu-id="63d8c-164">module</span></span>  
<span data-ttu-id="63d8c-165">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-165">A string data type that specifies a three-letter label file ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-166">Return Value</span></span>

<span data-ttu-id="63d8c-167">LabelBulkEditor クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="63d8c-167">An instance of the LabelBulkEditor class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-168">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-168">Remarks</span></span>

<span data-ttu-id="63d8c-169">LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-169">The LabelBulkEditor class is used to quickly modify a label file.</span></span> <span data-ttu-id="63d8c-170">このメソッドは、クライアント層から呼び出されたときに nullNothingnullptrunita null 参照 (Visual Basic ではNothing) を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-170">This method returns nullNothingnullptrunita null reference (Nothing in Visual Basic) when it is invoked from the client tier.</span></span>

### <a name="method-createlabelfile"></a><span data-ttu-id="63d8c-171">メソッド createLabelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-171">Method createLabelFile</span></span>

<span data-ttu-id="63d8c-172">指定されたラベル ID のラベル ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-172">Creates a label file for a specified label ID.</span></span>

    public boolean createLabelFile(str module, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-173">Parameters</span></span>

<span data-ttu-id="63d8c-174">モジュール</span><span class="sxs-lookup"><span data-stu-id="63d8c-174">module</span></span>  
<span data-ttu-id="63d8c-175">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-175">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-176">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-176">language</span></span>  
<span data-ttu-id="63d8c-177">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-177">A string data type that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-178">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-178">Return Value</span></span>

<span data-ttu-id="63d8c-179">ファイルが作成された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-179">true if a file is created; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-180">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-180">Remarks</span></span>

<span data-ttu-id="63d8c-181">ラベル ファイルは、ファイル バッファがディスクにフラッシュされた後に作成されます。これは、サーバーが閉じるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-181">The label file is created after the file buffers are flushed to disk, which occurs when the server closes.</span></span>

### <a name="method-delete"></a><span data-ttu-id="63d8c-182">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="63d8c-182">Method delete</span></span>

<span data-ttu-id="63d8c-183">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-183">Deletes a specified label.</span></span>

    public boolean delete(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-184">Parameters</span></span>

<span data-ttu-id="63d8c-185">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-185">label</span></span>  
<span data-ttu-id="63d8c-186">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-186">A string that specifies the label ID.</span></span> <span data-ttu-id="63d8c-187">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-187">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-188">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-188">Return Value</span></span>

<span data-ttu-id="63d8c-189">ラベル ID が削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-189">true if the label ID is deleted; otherwise, false.</span></span>

### <a name="method-exists"></a><span data-ttu-id="63d8c-190">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="63d8c-190">Method exists</span></span>

<span data-ttu-id="63d8c-191">指定したラベル ID が存在するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-191">Indicates whether a specified label ID exists.</span></span>

    public boolean exists(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-192">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-192">Parameters</span></span>

<span data-ttu-id="63d8c-193">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-193">label</span></span>  
<span data-ttu-id="63d8c-194">アット マーク (@) を含むラベル ID 文字列からの literalStr 関数の出力。</span><span class="sxs-lookup"><span data-stu-id="63d8c-194">The output of the literalStr function from a label ID string that includes the at sign (@).</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-195">Return Value</span></span>

<span data-ttu-id="63d8c-196">ラベル ID が存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-196">true if the label ID exists; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-197">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-197">Remarks</span></span>

<span data-ttu-id="63d8c-198">ラベル パラメーターの値の形式は、literalStr と同様でなければいけません ("@SYS24359")。</span><span class="sxs-lookup"><span data-stu-id="63d8c-198">The format of the label parameter value must resemble literalStr("@SYS24359").</span></span>

### <a name="method-extractcomment"></a><span data-ttu-id="63d8c-199">メソッド extractComment</span><span class="sxs-lookup"><span data-stu-id="63d8c-199">Method extractComment</span></span>

<span data-ttu-id="63d8c-200">指定されたラベル ID に関連付けられているコメントを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-200">Returns a comment that is associated with a specified label ID.</span></span>

    public str extractComment(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-201">Parameters</span></span>

<span data-ttu-id="63d8c-202">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-202">label</span></span>  
<span data-ttu-id="63d8c-203">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-203">A string that specifies the label ID.</span></span> <span data-ttu-id="63d8c-204">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-204">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-205">Return Value</span></span>

<span data-ttu-id="63d8c-206">指定されたラベル ID に関連付けられているコメントを示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-206">A string value that indicates the comment that is associated with the specified label ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-207">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-207">Remarks</span></span>

<span data-ttu-id="63d8c-208">存在しないラベル ID を指定する場合、このメソッドは文字列として指定した ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-208">If you specify a label ID that does not exist, this method returns the specified ID as a string.</span></span> <span data-ttu-id="63d8c-209">ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-209">If you do not include the @ in the label parameter value, the method returns the label ID.</span></span>

### <a name="method-extractstring"></a><span data-ttu-id="63d8c-210">メソッド extractString</span><span class="sxs-lookup"><span data-stu-id="63d8c-210">Method extractString</span></span>

<span data-ttu-id="63d8c-211">指定されたラベル ID に関連付けられているテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-211">Returns the text that is associated with a specified label ID.</span></span>

    public str extractString(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-212">Parameters</span></span>

<span data-ttu-id="63d8c-213">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-213">label</span></span>  
<span data-ttu-id="63d8c-214">ラベル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-214">A string data type that specifies a label ID.</span></span> <span data-ttu-id="63d8c-215">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-215">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-216">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-216">Return Value</span></span>

<span data-ttu-id="63d8c-217">指定されたラベル ID に関連付けられているテキストを示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-217">A string data type value that indicates the text that is associated with the specified label ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-218">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-218">Remarks</span></span>

<span data-ttu-id="63d8c-219">存在しないラベル ID を指定する場合、メソッドは文字列として指定した ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-219">If you specify a label ID that does not exist, the method returns the specified ID as a string.</span></span> <span data-ttu-id="63d8c-220">ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-220">If you do not include the @ in the label parameter value, the method returns the label ID.</span></span>

### <a name="method-getfirstlabelfile"></a><span data-ttu-id="63d8c-221">メソッド getFirstLabelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-221">Method getFirstLabelFile</span></span>

<span data-ttu-id="63d8c-222">最初のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-222">Returns the first label file ID record.</span></span>

    public str getFirstLabelFile()

#### <a name="return-value"></a><span data-ttu-id="63d8c-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-223">Return Value</span></span>

<span data-ttu-id="63d8c-224">ラベル ファイル ID を示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-224">A string data type value that indicates the label file ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-225">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-225">Remarks</span></span>

<span data-ttu-id="63d8c-226">ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-226">A label file ID is a three-letter identifier for a label file.</span></span>

### <a name="method-getlabelfilecreateddate"></a><span data-ttu-id="63d8c-227">メソッド getLabelFileCreatedDate</span><span class="sxs-lookup"><span data-stu-id="63d8c-227">Method getLabelFileCreatedDate</span></span>

<span data-ttu-id="63d8c-228">指定したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-228">Returns the date that a specified label file was created.</span></span>

    public Date getLabelFileCreatedDate(str labelFile, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-229">Parameters</span></span>

<span data-ttu-id="63d8c-230">labelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-230">labelFile</span></span>  
<span data-ttu-id="63d8c-231">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-231">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-232">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-232">language</span></span>  
<span data-ttu-id="63d8c-233">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-233">A string data type that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-234">Return Value</span></span>

<span data-ttu-id="63d8c-235">ラベル ファイルの作成日時を示す Date データ タイプ値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-235">A Date data type value that indicates when a label file is created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-236">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-236">Remarks</span></span>

<span data-ttu-id="63d8c-237">date2str 関数を使用すると日付をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-237">You can use the date2str function to convert the date to a text string.</span></span>

### <a name="method-getlabelfilecreatedtime"></a><span data-ttu-id="63d8c-238">メソッド getLabelFileCreatedTime</span><span class="sxs-lookup"><span data-stu-id="63d8c-238">Method getLabelFileCreatedTime</span></span>

<span data-ttu-id="63d8c-239">指定したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-239">Returns the time that a specified label file was created.</span></span>

    public int getLabelFileCreatedTime(str labelFile, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-240">Parameters</span></span>

<span data-ttu-id="63d8c-241">labelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-241">labelFile</span></span>  
<span data-ttu-id="63d8c-242">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-242">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-243">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-243">language</span></span>  
<span data-ttu-id="63d8c-244">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-244">A string data type that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-245">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-245">Return Value</span></span>

<span data-ttu-id="63d8c-246">ラベル ファイルが作成された時間を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-246">An integer data type value that indicates the time that a label file is created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-247">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-247">Remarks</span></span>

<span data-ttu-id="63d8c-248">詳細については、「方法: ラベル ファイルの作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63d8c-248">For more information, see How to: Create a Label File.</span></span> <span data-ttu-id="63d8c-249">time2str 関数を使用すると整数をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-249">You can use the time2str function to convert the integer to a text string.</span></span>

### <a name="method-getlabelfilemodificationdate"></a><span data-ttu-id="63d8c-250">メソッド getLabelFileModificationDate</span><span class="sxs-lookup"><span data-stu-id="63d8c-250">Method getLabelFileModificationDate</span></span>

<span data-ttu-id="63d8c-251">変更したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-251">Returns the date that a specified label file was modified.</span></span>

    public Date getLabelFileModificationDate(str labelFile, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-252">Parameters</span></span>

<span data-ttu-id="63d8c-253">labelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-253">labelFile</span></span>  
<span data-ttu-id="63d8c-254">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-254">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-255">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-255">language</span></span>  
<span data-ttu-id="63d8c-256">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-256">A string data type that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-257">Return Value</span></span>

<span data-ttu-id="63d8c-258">ラベル ファイルの変更日時を示す Date データ タイプ値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-258">A Date data type value that indicates when a label file was modified.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-259">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-259">Remarks</span></span>

<span data-ttu-id="63d8c-260">date2str 関数を使用すると日付をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-260">You can use the date2str function to convert the date to a text string.</span></span>

### <a name="method-getlabelfilemodificationtime"></a><span data-ttu-id="63d8c-261">メソッド getLabelFileModificationTime</span><span class="sxs-lookup"><span data-stu-id="63d8c-261">Method getLabelFileModificationTime</span></span>

<span data-ttu-id="63d8c-262">変更したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-262">Returns the time that a specified label file was modified.</span></span>

    public int getLabelFileModificationTime(str labelFile, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-263">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-263">Parameters</span></span>

<span data-ttu-id="63d8c-264">labelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-264">labelFile</span></span>  
<span data-ttu-id="63d8c-265">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-265">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-266">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-266">language</span></span>  
<span data-ttu-id="63d8c-267">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-267">A string data type that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-268">Return Value</span></span>

<span data-ttu-id="63d8c-269">ラベル ファイルが変更された時間を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-269">An integer value that indicates the time that a label file was modified.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-270">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-270">Remarks</span></span>

<span data-ttu-id="63d8c-271">time2str 関数を使用すると整数をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-271">You can use the time2str function to convert the integer to a text string.</span></span>

### <a name="method-getnextlabelfile"></a><span data-ttu-id="63d8c-272">メソッド getNextLabelFile</span><span class="sxs-lookup"><span data-stu-id="63d8c-272">Method getNextLabelFile</span></span>

<span data-ttu-id="63d8c-273">次のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-273">Returns the next label file ID record.</span></span>

    public str getNextLabelFile()

#### <a name="return-value"></a><span data-ttu-id="63d8c-274">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-274">Return Value</span></span>

<span data-ttu-id="63d8c-275">ラベル ファイル ID を示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-275">A string data type value that indicates the label file ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-276">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-276">Remarks</span></span>

<span data-ttu-id="63d8c-277">ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-277">A label file ID is a three-letter identifier for a label file.</span></span>

### <a name="method-insert"></a><span data-ttu-id="63d8c-278">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="63d8c-278">Method insert</span></span>

<span data-ttu-id="63d8c-279">指定されたテキスト文字列のラベル ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-279">Creates a label ID for a specified text string.</span></span>

    public str insert(str text, str comment, str module)

#### <a name="parameters"></a><span data-ttu-id="63d8c-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-280">Parameters</span></span>

<span data-ttu-id="63d8c-281">テキスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-281">text</span></span>  
<span data-ttu-id="63d8c-282">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-282">A string data type that specifies a three-letter label file ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-283">comment</span><span class="sxs-lookup"><span data-stu-id="63d8c-283">comment</span></span>  
<span data-ttu-id="63d8c-284">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-284">A string data type that specifies a three-letter label file ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-285">モジュール</span><span class="sxs-lookup"><span data-stu-id="63d8c-285">module</span></span>  
<span data-ttu-id="63d8c-286">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-286">A string data type that specifies a three-letter label file ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-287">Return Value</span></span>

<span data-ttu-id="63d8c-288">作成されるラベル ID の文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-288">A string data type value for the label ID that is created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-289">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-289">Remarks</span></span>

<span data-ttu-id="63d8c-290">この操作では、すべての言語に新しいラベル ID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-290">This operation allocates a new label ID across all languages.</span></span>

### <a name="method-labelid"></a><span data-ttu-id="63d8c-291">メソッド labelId</span><span class="sxs-lookup"><span data-stu-id="63d8c-291">Method labelId</span></span>

<span data-ttu-id="63d8c-292">指定したラベル ID に含まれる番号を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-292">Returns the number that is included in a specified label ID.</span></span>

    public int labelId(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-293">Parameters</span></span>

<span data-ttu-id="63d8c-294">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-294">label</span></span>  
<span data-ttu-id="63d8c-295">ラベル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="63d8c-295">A string data type that specifies the label ID.</span></span> <span data-ttu-id="63d8c-296">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-296">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-297">Return Value</span></span>

<span data-ttu-id="63d8c-298">ラベル ID に含まれる番号を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-298">An integer data type value that indicates the number that is included in a label ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-299">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-299">Remarks</span></span>

<span data-ttu-id="63d8c-300">searchFirst または searchNext メソッドを呼び出してから、パラメーターとして戻り値をこのメソッドに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-300">You must call the searchFirst or searchNext method, and then pass the return value as a parameter to this method.</span></span>

### <a name="method-maxlabelid"></a><span data-ttu-id="63d8c-301">メソッド maxLabelId</span><span class="sxs-lookup"><span data-stu-id="63d8c-301">Method maxLabelId</span></span>

<span data-ttu-id="63d8c-302">指定したラベル ファイル内の最後のラベルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-302">Returns the ID for the last label in the specified label file.</span></span>

    public int maxLabelId(str module)

#### <a name="parameters"></a><span data-ttu-id="63d8c-303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-303">Parameters</span></span>

<span data-ttu-id="63d8c-304">モジュール</span><span class="sxs-lookup"><span data-stu-id="63d8c-304">module</span></span>  
<span data-ttu-id="63d8c-305">3 文字のラベル ファイル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-305">A string that specifies a three-letter label file ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-306">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-306">Return Value</span></span>

<span data-ttu-id="63d8c-307">指定したラベル ファイルの最大ラベル ID を示す整数。</span><span class="sxs-lookup"><span data-stu-id="63d8c-307">An integer that indicates the maximum label ID for the specified label file.</span></span>

### <a name="method-modify"></a><span data-ttu-id="63d8c-308">メソッド modify</span><span class="sxs-lookup"><span data-stu-id="63d8c-308">Method modify</span></span>

<span data-ttu-id="63d8c-309">指定されたラベルに関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-309">Modifies the text and comment that are associated with a specified label.</span></span>

    public boolean modify(str label, str text, [str comment])

#### <a name="parameters"></a><span data-ttu-id="63d8c-310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-310">Parameters</span></span>

<span data-ttu-id="63d8c-311">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-311">label</span></span>  
<span data-ttu-id="63d8c-312">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-312">A string that specifies the comment that is associated with a label ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-313">テキスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-313">text</span></span>  
<span data-ttu-id="63d8c-314">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-314">A string that specifies the comment that is associated with a label ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-315">comment</span><span class="sxs-lookup"><span data-stu-id="63d8c-315">comment</span></span>  
<span data-ttu-id="63d8c-316">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-316">A string that specifies the comment that is associated with a label ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-317">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-317">Return Value</span></span>

<span data-ttu-id="63d8c-318">ラベル ID が修正された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-318">true if the label ID is modified; otherwise, false.</span></span>

### <a name="method-moduleid"></a><span data-ttu-id="63d8c-319">メソッド moduleId</span><span class="sxs-lookup"><span data-stu-id="63d8c-319">Method moduleId</span></span>

<span data-ttu-id="63d8c-320">指定したラベル ID のラベル ファイルを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-320">Returns the label file ID for a specified label ID.</span></span>

    public str moduleId(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-321">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-321">Parameters</span></span>

<span data-ttu-id="63d8c-322">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-322">label</span></span>  
<span data-ttu-id="63d8c-323">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-323">A string that specifies the label ID.</span></span> <span data-ttu-id="63d8c-324">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-324">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-325">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-325">Return Value</span></span>

<span data-ttu-id="63d8c-326">指定したラベル ID のラベル ファイル ID を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-326">A string that indicates the label file ID for a specified label ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-327">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-327">Remarks</span></span>

<span data-ttu-id="63d8c-328">SearchFirst または searchNext のメソッドを呼び出すパラメーターとして戻り値を labelId メソッドに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-328">You need to call the searchFirst or searchNext method, and then pass the return value as a parameter to the labelId method.</span></span>

### <a name="method-morelabelfiles"></a><span data-ttu-id="63d8c-329">メソッド moreLabelFiles</span><span class="sxs-lookup"><span data-stu-id="63d8c-329">Method moreLabelFiles</span></span>

<span data-ttu-id="63d8c-330">追加のラベル ファイルがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-330">Indicates whether there are additional label files.</span></span>

    public boolean moreLabelFiles()

#### <a name="return-value"></a><span data-ttu-id="63d8c-331">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-331">Return Value</span></span>

<span data-ttu-id="63d8c-332">追加のラベル ファイルがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-332">true if there are additional label files; otherwise, false.</span></span>

### <a name="method-name"></a><span data-ttu-id="63d8c-333">メソッド名</span><span class="sxs-lookup"><span data-stu-id="63d8c-333">Method name</span></span>

<span data-ttu-id="63d8c-334">指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-334">Returns a label ID, based on a specified label file ID and label ID number.</span></span>

    public str name(str module, int labelId)

#### <a name="parameters"></a><span data-ttu-id="63d8c-335">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-335">Parameters</span></span>

<span data-ttu-id="63d8c-336">モジュール</span><span class="sxs-lookup"><span data-stu-id="63d8c-336">module</span></span>  
<span data-ttu-id="63d8c-337">ラベル ID の数値部分を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="63d8c-337">An integer that specifies the numeric part of a label ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-338">labelId</span><span class="sxs-lookup"><span data-stu-id="63d8c-338">labelId</span></span>  
<span data-ttu-id="63d8c-339">ラベル ID の数値部分を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="63d8c-339">An integer that specifies the numeric part of a label ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-340">Return Value</span></span>

<span data-ttu-id="63d8c-341">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-341">A string value that indicates the label ID.</span></span>

### <a name="method-searchfirst"></a><span data-ttu-id="63d8c-342">メソッド searchFirst</span><span class="sxs-lookup"><span data-stu-id="63d8c-342">Method searchFirst</span></span>

<span data-ttu-id="63d8c-343">指定した検索用語で検出された最初のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-343">Returns the first label ID that is found for a specified search term.</span></span>

    public str searchFirst(str searchString)

#### <a name="parameters"></a><span data-ttu-id="63d8c-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-344">Parameters</span></span>

<span data-ttu-id="63d8c-345">searchString</span><span class="sxs-lookup"><span data-stu-id="63d8c-345">searchString</span></span>  
<span data-ttu-id="63d8c-346">検索用語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-346">A string that specifies the search term.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-347">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-347">Return Value</span></span>

<span data-ttu-id="63d8c-348">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-348">A string value that indicates the label ID.</span></span>

### <a name="method-searchnext"></a><span data-ttu-id="63d8c-349">メソッド searchNext</span><span class="sxs-lookup"><span data-stu-id="63d8c-349">Method searchNext</span></span>

<span data-ttu-id="63d8c-350">searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-350">Returns the next label ID that is found for a search term that is passed to the searchFirst method.</span></span>

    public str searchNext()

#### <a name="return-value"></a><span data-ttu-id="63d8c-351">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-351">Return Value</span></span>

<span data-ttu-id="63d8c-352">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-352">A string value that indicates the label ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-353">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-353">Remarks</span></span>

<span data-ttu-id="63d8c-354">このメソッドを呼び出す前に、searchFirst メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-354">You must call the searchFirst method before you call this method.</span></span> <span data-ttu-id="63d8c-355">それ以外の場合、このメソッドは、ランダムなラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-355">Otherwise, this method returns a random label ID.</span></span>

### <a name="method-flush"></a><span data-ttu-id="63d8c-356">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="63d8c-356">Method flush</span></span>

<span data-ttu-id="63d8c-357">ディスクにラベル ファイル バッファーをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-357">Flushes the label file buffers to disk.</span></span>

    public static boolean flush(str labelFileId, str language)

#### <a name="parameters"></a><span data-ttu-id="63d8c-358">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-358">Parameters</span></span>

<span data-ttu-id="63d8c-359">labelFileId</span><span class="sxs-lookup"><span data-stu-id="63d8c-359">labelFileId</span></span>  
<span data-ttu-id="63d8c-360">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-360">A string that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="63d8c-361">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-361">language</span></span>  
<span data-ttu-id="63d8c-362">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-362">A string that specifies a language by using a language prefix.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-363">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="63d8c-364">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-364">Method new</span></span>

<span data-ttu-id="63d8c-365">ラベル クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-365">Creates a new instance of the Label class.</span></span>

    public void new([str language])

#### <a name="parameters"></a><span data-ttu-id="63d8c-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-366">Parameters</span></span>

<span data-ttu-id="63d8c-367">言語</span><span class="sxs-lookup"><span data-stu-id="63d8c-367">language</span></span>  
<span data-ttu-id="63d8c-368">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-368">A string that specifies a language by using a language prefix.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="63d8c-369">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="63d8c-369">Method finalize</span></span>

<span data-ttu-id="63d8c-370">現在のラベル ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-370">Closes the current label file.</span></span>

    public void finalize()

## <a name="class-labelbulkeditor"></a><span data-ttu-id="63d8c-371">クラス LabelBulkEditor</span><span class="sxs-lookup"><span data-stu-id="63d8c-371">Class LabelBulkEditor</span></span>
    class LabelBulkEditor extends Object

<span data-ttu-id="63d8c-372">LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-372">The LabelBulkEditor class is used to quickly modify label files.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-373">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-373">Remarks</span></span>

<span data-ttu-id="63d8c-374">LabelBulkEditor クラスは、Label.bulkEditor() メソッドを通じてインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-374">The LabelBulkEditor class is instantiated through the Label.bulkEditor() method.</span></span> <span data-ttu-id="63d8c-375">ラベル ファイルは、クラスのインスタンスが作成されたときに変更用に開かれ、インスタンスがガベージ コレクションされたときにラベル ファイルは閉じられます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-375">The label file is opened for modification when the instance of the class is created, and the label file is closed when the instance has garbage collected.</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-376">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-376">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-377">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-377">Methods</span></span>

| <span data-ttu-id="63d8c-378">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-378">Method</span></span>                                                      | <span data-ttu-id="63d8c-379">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-379">Description</span></span>                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-380">public boolean delete(str label)</span><span class="sxs-lookup"><span data-stu-id="63d8c-380">public boolean delete(str label)</span></span>                            | <span data-ttu-id="63d8c-381">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-381">Deletes a specified label.</span></span>                                                   |
| <span data-ttu-id="63d8c-382">public boolean modify(str label, str text, \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-382">public boolean modify(str label, str text, \[str comment\])</span></span> | <span data-ttu-id="63d8c-383">指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-383">Modifies the text and comment that are associated with a specified label ID.</span></span> |
| <span data-ttu-id="63d8c-384">public void new()</span><span class="sxs-lookup"><span data-stu-id="63d8c-384">public void new()</span></span>                                           | <span data-ttu-id="63d8c-385">LabelBulkEditor クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-385">Initializes an instance of the LabelBulkEditor class.</span></span>                        |

### <a name="method-delete"></a><span data-ttu-id="63d8c-386">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="63d8c-386">Method delete</span></span>

<span data-ttu-id="63d8c-387">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-387">Deletes a specified label.</span></span>

    public boolean delete(str label)

#### <a name="parameters"></a><span data-ttu-id="63d8c-388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-388">Parameters</span></span>

<span data-ttu-id="63d8c-389">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-389">label</span></span>  
<span data-ttu-id="63d8c-390">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-390">A string that specifies the label ID.</span></span> <span data-ttu-id="63d8c-391">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-391">The string must include an at sign (@) followed by a label file ID and a number.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-392">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-392">Return Value</span></span>

<span data-ttu-id="63d8c-393">ラベルが削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-393">true if the label is deleted; otherwise, false.</span></span>

### <a name="method-modify"></a><span data-ttu-id="63d8c-394">メソッド modify</span><span class="sxs-lookup"><span data-stu-id="63d8c-394">Method modify</span></span>

<span data-ttu-id="63d8c-395">指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-395">Modifies the text and comment that are associated with a specified label ID.</span></span>

    public boolean modify(str label, str text, [str comment])

#### <a name="parameters"></a><span data-ttu-id="63d8c-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-396">Parameters</span></span>

<span data-ttu-id="63d8c-397">ラベル</span><span class="sxs-lookup"><span data-stu-id="63d8c-397">label</span></span>  
<span data-ttu-id="63d8c-398">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-398">A string that specifies the comment that is associated with the label ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-399">テキスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-399">text</span></span>  
<span data-ttu-id="63d8c-400">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-400">A string that specifies the comment that is associated with the label ID.</span></span>

<!-- -->

<span data-ttu-id="63d8c-401">comment</span><span class="sxs-lookup"><span data-stu-id="63d8c-401">comment</span></span>  
<span data-ttu-id="63d8c-402">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-402">A string that specifies the comment that is associated with the label ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-403">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-403">Return Value</span></span>

<span data-ttu-id="63d8c-404">ラベルが修正された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-404">true if the label is modified; otherwise, false.</span></span>

### <a name="method-new"></a><span data-ttu-id="63d8c-405">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-405">Method new</span></span>

<span data-ttu-id="63d8c-406">LabelBulkEditor クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-406">Initializes an instance of the LabelBulkEditor class.</span></span>

    public void new()

## <a name="class-lastaotselection"></a><span data-ttu-id="63d8c-407">クラス LastAotSelection</span><span class="sxs-lookup"><span data-stu-id="63d8c-407">Class LastAotSelection</span></span>
    class LastAotSelection extends Object

### <a name="remarks"></a><span data-ttu-id="63d8c-408">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-408">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-409">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-409">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-410">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-410">Methods</span></span>

| <span data-ttu-id="63d8c-411">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-411">Method</span></span>                           | <span data-ttu-id="63d8c-412">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-412">Description</span></span>                                               |
|----------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="63d8c-413">public TreeNode first()</span><span class="sxs-lookup"><span data-stu-id="63d8c-413">public TreeNode first()</span></span>          |                                                           |
| <span data-ttu-id="63d8c-414">public TreeNode next()</span><span class="sxs-lookup"><span data-stu-id="63d8c-414">public TreeNode next()</span></span>           |                                                           |
| <span data-ttu-id="63d8c-415">public ProjectNode projectRoot()</span><span class="sxs-lookup"><span data-stu-id="63d8c-415">public ProjectNode projectRoot()</span></span> |                                                           |
| <span data-ttu-id="63d8c-416">public int selectionCount()</span><span class="sxs-lookup"><span data-stu-id="63d8c-416">public int selectionCount()</span></span>      |                                                           |
| <span data-ttu-id="63d8c-417">public void new()</span><span class="sxs-lookup"><span data-stu-id="63d8c-417">public void new()</span></span>                | <span data-ttu-id="63d8c-418">LastAotSelection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-418">Initializes a new instance of the LastAotSelection class.</span></span> |
| <span data-ttu-id="63d8c-419">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="63d8c-419">public void finalize()</span></span>           |                                                           |

### <a name="method-first"></a><span data-ttu-id="63d8c-420">メソッド first</span><span class="sxs-lookup"><span data-stu-id="63d8c-420">Method first</span></span>

    public TreeNode first()

#### <a name="return-value"></a><span data-ttu-id="63d8c-421">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-421">Return Value</span></span>

### <a name="method-next"></a><span data-ttu-id="63d8c-422">メソッド next</span><span class="sxs-lookup"><span data-stu-id="63d8c-422">Method next</span></span>

    public TreeNode next()

#### <a name="return-value"></a><span data-ttu-id="63d8c-423">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-423">Return Value</span></span>

### <a name="method-projectroot"></a><span data-ttu-id="63d8c-424">メソッド projectRoot</span><span class="sxs-lookup"><span data-stu-id="63d8c-424">Method projectRoot</span></span>

    public ProjectNode projectRoot()

#### <a name="return-value"></a><span data-ttu-id="63d8c-425">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-425">Return Value</span></span>

### <a name="method-selectioncount"></a><span data-ttu-id="63d8c-426">メソッド selectionCount</span><span class="sxs-lookup"><span data-stu-id="63d8c-426">Method selectionCount</span></span>

    public int selectionCount()

#### <a name="return-value"></a><span data-ttu-id="63d8c-427">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-427">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="63d8c-428">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-428">Method new</span></span>

<span data-ttu-id="63d8c-429">LastAotSelection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-429">Initializes a new instance of the LastAotSelection class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="63d8c-430">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="63d8c-430">Method finalize</span></span>

    public void finalize()

## <a name="class-list"></a><span data-ttu-id="63d8c-431">クラス リスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-431">Class List</span></span>
    class List extends Object

<span data-ttu-id="63d8c-432">順にアクセスされる任意の数の要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-432">Contains any number of elements that are accessed sequentially.</span></span> <span data-ttu-id="63d8c-433">リストは、あらゆる X++ 型の値を含めることができる構造です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-433">Lists are structures that can contain values of any X++ type.</span></span> <span data-ttu-id="63d8c-434">リスト内のすべての値は同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-434">All the values in the list must be of the same type.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-435">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-435">Remarks</span></span>

<span data-ttu-id="63d8c-436">リスト内の値のタイプは、リストが作成されたときに指定され、後で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="63d8c-436">The type of the values in the list is specified when the list is created and cannot be changed afterwards.</span></span> <span data-ttu-id="63d8c-437">リストの実装は、リスト要素のトラバーサルを非常に高速にします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-437">The implementation of lists makes traversal of the list elements very fast.</span></span> <span data-ttu-id="63d8c-438">リストを移動するには、ListEnumerator クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-438">Lists can be traversed by using the ListEnumerator class.</span></span> <span data-ttu-id="63d8c-439">ListEnumerator オブジェクトを作成するには、List.getEnumerator を使用します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-439">To create a ListEnumerator object, use List.getEnumerator.</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-440">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-440">Examples</span></span>

<span data-ttu-id="63d8c-441">次の例では、整数のリストを作成し、リストの説明とそれに含まれる値を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-441">The following example creates a list of integers and prints out a description of the list and the values that it contains.</span></span>

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="63d8c-442">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-442">Methods</span></span>

| <span data-ttu-id="63d8c-443">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-443">Method</span></span>                                                | <span data-ttu-id="63d8c-444">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-444">Description</span></span>                                                                           |
|-------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-445">public AnyType addEnd(AnyType element)</span><span class="sxs-lookup"><span data-stu-id="63d8c-445">public AnyType addEnd(AnyType element)</span></span>                | <span data-ttu-id="63d8c-446">リストの末尾に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-446">Adds a value to the end of the list.</span></span>                                                  |
| <span data-ttu-id="63d8c-447">public AnyType addStart(AnyType element)</span><span class="sxs-lookup"><span data-stu-id="63d8c-447">public AnyType addStart(AnyType element)</span></span>              | <span data-ttu-id="63d8c-448">リストの冒頭に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-448">Adds a value to the start of the list.</span></span>                                                |
| <span data-ttu-id="63d8c-449">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-449">public str definitionString()</span></span>                         | <span data-ttu-id="63d8c-450">リスト内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-450">Returns a description of the type of the elements in the list.</span></span>                        |
| <span data-ttu-id="63d8c-451">public int elements()</span><span class="sxs-lookup"><span data-stu-id="63d8c-451">public int elements()</span></span>                                 | <span data-ttu-id="63d8c-452">リスト内の要素の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-452">Specifies the number of elements in a list.</span></span>                                           |
| <span data-ttu-id="63d8c-453">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="63d8c-453">public boolean empty()</span></span>                                | <span data-ttu-id="63d8c-454">一覧が空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-454">Determines whether a list is empty.</span></span>                                                   |
| <span data-ttu-id="63d8c-455">public boolean equalTo(List l)</span><span class="sxs-lookup"><span data-stu-id="63d8c-455">public boolean equalTo(List l)</span></span>                        | <span data-ttu-id="63d8c-456">一覧が現在の一覧と同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-456">Determines whether a list is the same as the current list.</span></span>                            |
| <span data-ttu-id="63d8c-457">public ListEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="63d8c-457">public ListEnumerator getEnumerator()</span></span>                 | <span data-ttu-id="63d8c-458">リストのスキャンを可能にするリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-458">Creates an enumerator for a list which allows you to traverse the list.</span></span>               |
| <span data-ttu-id="63d8c-459">public container pack()</span><span class="sxs-lookup"><span data-stu-id="63d8c-459">public container pack()</span></span>                               | <span data-ttu-id="63d8c-460">List クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-460">Serializes the current instance of the List class.</span></span>                                    |
| <span data-ttu-id="63d8c-461">public str toString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-461">public str toString()</span></span>                                 | <span data-ttu-id="63d8c-462">リスト内の値の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-462">Returns a description of the values in the list.</span></span>                                      |
| <span data-ttu-id="63d8c-463">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="63d8c-463">public Types typeId()</span></span>                                 | <span data-ttu-id="63d8c-464">リスト内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-464">Returns the type of the values in a list.</span></span>                                             |
| <span data-ttu-id="63d8c-465">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-465">public str xml(\[int indent\])</span></span>                        | <span data-ttu-id="63d8c-466">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-466">Returns an XML string that represents the current object.</span></span>                             |
| <span data-ttu-id="63d8c-467">::public static List create(container container)</span><span class="sxs-lookup"><span data-stu-id="63d8c-467">::public static List create(container container)</span></span>      | <span data-ttu-id="63d8c-468">以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-468">Creates a list from the container obtained from a prior call to the List.pack method.</span></span> |
| <span data-ttu-id="63d8c-469">::public static List createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="63d8c-469">::public static List createFromXML(Object xmlnode)</span></span>    |                                                                                       |
| <span data-ttu-id="63d8c-470">::public static boolean equal(List list1, List list2)</span><span class="sxs-lookup"><span data-stu-id="63d8c-470">::public static boolean equal(List list1, List list2)</span></span> | <span data-ttu-id="63d8c-471">2 つのリストが同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-471">Determines whether two lists are identical.</span></span>                                           |
| <span data-ttu-id="63d8c-472">::public static List merge(List list1, List list2)</span><span class="sxs-lookup"><span data-stu-id="63d8c-472">::public static List merge(List list1, List list2)</span></span>    | <span data-ttu-id="63d8c-473">2 つのリストを組み合わせ、新しいリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-473">Combines two lists to create a new list.</span></span>                                              |
| <span data-ttu-id="63d8c-474">public void appendList(List list)</span><span class="sxs-lookup"><span data-stu-id="63d8c-474">public void appendList(List list)</span></span>                     |                                                                                       |
| <span data-ttu-id="63d8c-475">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="63d8c-475">public void new(Types Type)</span></span>                           | <span data-ttu-id="63d8c-476">リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-476">Creates a list.</span></span>                                                                       |

### <a name="method-addend"></a><span data-ttu-id="63d8c-477">メソッド addEnd</span><span class="sxs-lookup"><span data-stu-id="63d8c-477">Method addEnd</span></span>

<span data-ttu-id="63d8c-478">リストの末尾に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-478">Adds a value to the end of the list.</span></span>

    public AnyType addEnd(AnyType element)

#### <a name="parameters"></a><span data-ttu-id="63d8c-479">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-479">Parameters</span></span>

<span data-ttu-id="63d8c-480">要素</span><span class="sxs-lookup"><span data-stu-id="63d8c-480">element</span></span>  
<span data-ttu-id="63d8c-481">リストの末尾に追加する値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-481">The value to add to the end of the list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-482">Return Value</span></span>

<span data-ttu-id="63d8c-483">リストに追加される値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-483">The value that is added to the list.</span></span>

### <a name="method-addstart"></a><span data-ttu-id="63d8c-484">メソッド addStart</span><span class="sxs-lookup"><span data-stu-id="63d8c-484">Method addStart</span></span>

<span data-ttu-id="63d8c-485">リストの冒頭に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-485">Adds a value to the start of the list.</span></span>

    public AnyType addStart(AnyType element)

#### <a name="parameters"></a><span data-ttu-id="63d8c-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-486">Parameters</span></span>

<span data-ttu-id="63d8c-487">要素</span><span class="sxs-lookup"><span data-stu-id="63d8c-487">element</span></span>  
<span data-ttu-id="63d8c-488">リストの冒頭に追加する値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-488">The value to add to the start of the list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-489">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-489">Return Value</span></span>

<span data-ttu-id="63d8c-490">このリストに追加される値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-490">The value added to the list.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-491">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-491">Remarks</span></span>

<span data-ttu-id="63d8c-492">要素は、List.addEnd メソッドを使用して、リストの最後に追加できます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-492">Elements can be added to the end of the list by using the List.addEnd method.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-493">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-493">Examples</span></span>

<span data-ttu-id="63d8c-494">次の例では、整数のリストを作成し、値の 1 と 2 をリストの末尾に追加し、値 3 をリストの先頭に追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-494">The following example creates a list of integers, adds the values 1 and 2 to the end of the list, and then adds the value 3 to the start of the list.</span></span> <span data-ttu-id="63d8c-495">List.toString メソッドによって返される値は {3, 1, 2} です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-495">The values that are returned by the List.toString method are {3, 1, 2}.</span></span>

    { 
        // Create a list of integers 
        list il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list. 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-definitionstring"></a><span data-ttu-id="63d8c-496">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="63d8c-496">Method definitionString</span></span>

<span data-ttu-id="63d8c-497">リスト内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-497">Returns a description of the type of the elements in the list.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-498">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-498">Return Value</span></span>

<span data-ttu-id="63d8c-499">リストの定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-499">A string that contains a definition of the list.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-500">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-500">Remarks</span></span>

<span data-ttu-id="63d8c-501">たとえば、このメソッドは、「int の一覧」を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-501">For example, this method could return "list of int".</span></span> <span data-ttu-id="63d8c-502">リスト内の値の一覧を印刷するには、List.toString メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-502">To print a list of the values within the list, use the List.toString method.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-503">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-503">Examples</span></span>

<span data-ttu-id="63d8c-504">次の例では、整数のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-504">The following example creates a list of integers.</span></span> <span data-ttu-id="63d8c-505">definitionString メソッドを使用して、リストの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-505">The definitionString method is used to print a description of the list.</span></span>

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description ofvthe list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-elements"></a><span data-ttu-id="63d8c-506">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="63d8c-506">Method elements</span></span>

<span data-ttu-id="63d8c-507">リスト内の要素の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-507">Specifies the number of elements in a list.</span></span>

    public int elements()

#### <a name="return-value"></a><span data-ttu-id="63d8c-508">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-508">Return Value</span></span>

<span data-ttu-id="63d8c-509">リスト内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="63d8c-509">The number of elements in the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-510">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-510">Examples</span></span>

<span data-ttu-id="63d8c-511">次の例では、整数のリストを作成し、いくつかの要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-511">The following example creates a list of integers and adds some elements to it.</span></span> <span data-ttu-id="63d8c-512">要素メソッドは、リストに 3 つの要素があるかどうかをテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-512">The elements method is used to test whether there are three elements in the list.</span></span>

    { 
        List il = new List(Types::Integer); 
        il.addStart(1); 
        il.addStart(2); 
        il.addStart(3); 
        if (il.elements() != 3) 
        { 
            print "Something is wrong..."; 
        } 
    }

### <a name="method-empty"></a><span data-ttu-id="63d8c-513">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="63d8c-513">Method empty</span></span>

<span data-ttu-id="63d8c-514">一覧が空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-514">Determines whether a list is empty.</span></span>

    public boolean empty()

#### <a name="return-value"></a><span data-ttu-id="63d8c-515">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-515">Return Value</span></span>

<span data-ttu-id="63d8c-516">リストが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-516">true if the list is empty; otherwise, false.</span></span>

### <a name="method-equalto"></a><span data-ttu-id="63d8c-517">メソッド equalTo</span><span class="sxs-lookup"><span data-stu-id="63d8c-517">Method equalTo</span></span>

<span data-ttu-id="63d8c-518">一覧が現在の一覧と同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-518">Determines whether a list is the same as the current list.</span></span>

    public boolean equalTo(List l)

#### <a name="parameters"></a><span data-ttu-id="63d8c-519">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-519">Parameters</span></span>

<span data-ttu-id="63d8c-520">l</span><span class="sxs-lookup"><span data-stu-id="63d8c-520">l</span></span>  
<span data-ttu-id="63d8c-521">現在のリストと比較されるリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-521">The list to be compared with the current list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-522">Return Value</span></span>

<span data-ttu-id="63d8c-523">指定したリストが、メソッドが呼び出されたリストと同一である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-523">true if the specified list is identical to the list on which the method is called; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-524">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-524">Remarks</span></span>

<span data-ttu-id="63d8c-525">2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-525">A list is equal to another list if the two lists are the same type, contain the same number of elements, and the elements occur in the same order.</span></span> <span data-ttu-id="63d8c-526">equalTo メソッドは、List.equal メソッドを使用するためのショートカットです。(this、l) と等しい。</span><span class="sxs-lookup"><span data-stu-id="63d8c-526">The equalTo method is a shortcut for using the List.equal method: equal(this, l).</span></span>

### <a name="method-getenumerator"></a><span data-ttu-id="63d8c-527">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="63d8c-527">Method getEnumerator</span></span>

<span data-ttu-id="63d8c-528">リストのスキャンを可能にするリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-528">Creates an enumerator for a list which allows you to traverse the list.</span></span>

    public ListEnumerator getEnumerator()

#### <a name="return-value"></a><span data-ttu-id="63d8c-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-529">Return Value</span></span>

<span data-ttu-id="63d8c-530">現在のリストの listEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-530">A listEnumerator object for the current list.</span></span>

### <a name="method-pack"></a><span data-ttu-id="63d8c-531">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="63d8c-531">Method pack</span></span>

<span data-ttu-id="63d8c-532">List クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-532">Serializes the current instance of the List class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="63d8c-533">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-533">Return Value</span></span>

<span data-ttu-id="63d8c-534">List クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="63d8c-534">A container that contains the current instance of the List class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-535">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-535">Remarks</span></span>

<span data-ttu-id="63d8c-536">このメソッドで作成されたコンテナーには、リストの最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-536">The container created by this method contains 3 elements before the first element from the list:</span></span>

-   <span data-ttu-id="63d8c-537">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="63d8c-537">A version number for the container</span></span>
-   <span data-ttu-id="63d8c-538">リスト要素のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="63d8c-538">An integer that identifies the data type of the list elements</span></span>
-   <span data-ttu-id="63d8c-539">リスト内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="63d8c-539">The number of elements in the list</span></span>

<span data-ttu-id="63d8c-540">リスト内の要素がオブジェクトとなっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-540">If the elements in the list are objects, packing is performed by calling the pack method successively on each object to yield a subcontainer.</span></span> <span data-ttu-id="63d8c-541">List.create メソッドを使用して、パックされたコンテナーからリストを取得できます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-541">The list can be retrieved from the packed container by using the List.create method.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-542">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-542">Examples</span></span>

<span data-ttu-id="63d8c-543">次の例では、レコードのリストを作成し、新しい projReverseMarking オブジェクトを作成するためのパラメーターとしてパックされたリストに渡します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-543">The following example creates a list of records and passes in the packed list as a parameter for creating a new projReverseMarking object.</span></span>

    public boolean canClose() 
    { 
        ProjReverseMarking      projReverseMarking; 
        boolean                 canClose; 
        List                    list; 
        canClose = super(); 
        if (element.closedOk() && canClose) 
        { 
            List = new List(Types::Record); 
            while select tmpFrmVirtualLines 
            { 
                list.addEnd(tmpFrmVirtualLines); 
            } 
            projReverseMarking = new ProjReverseMarking(list.pack()); 
            projReverseMarking.run(); 
        } 
        return canClose; 
    }

### <a name="method-tostring"></a><span data-ttu-id="63d8c-544">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="63d8c-544">Method toString</span></span>

<span data-ttu-id="63d8c-545">リスト内の値の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-545">Returns a description of the values in the list.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-546">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-546">Return Value</span></span>

<span data-ttu-id="63d8c-547">リストの要素の値を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-547">A string that describes the values of the elements in the list.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-548">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-548">Remarks</span></span>

<span data-ttu-id="63d8c-549">リスト内の要素のタイプの説明を印刷するには、List.definitionString メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-549">To print a description of the type of the elements in the list, use the List.definitionString method.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-550">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-550">Examples</span></span>

<span data-ttu-id="63d8c-551">次の例では、整数のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-551">The following example creates a list of integers.</span></span> <span data-ttu-id="63d8c-552">toString メソッドを使用して、リストにある値の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-552">The toString method is used to print a description of the values in the list.</span></span>

    { 
        // Create a list of integers 
        List il = new List(Types::Integer); 
        // Add some elements to the list 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addStart(3); 
        // Print a description of the list 
        print il.definitionString(); 
        print il.toString(); 
        pause; 
    }

### <a name="method-typeid"></a><span data-ttu-id="63d8c-553">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="63d8c-553">Method typeId</span></span>

<span data-ttu-id="63d8c-554">リスト内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-554">Returns the type of the values in a list.</span></span>

    public Types typeId()

#### <a name="return-value"></a><span data-ttu-id="63d8c-555">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-555">Return Value</span></span>

<span data-ttu-id="63d8c-556">リスト要素のタイプ。</span><span class="sxs-lookup"><span data-stu-id="63d8c-556">The type of the list elements.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-557">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-557">Remarks</span></span>

<span data-ttu-id="63d8c-558">リストのタイプは、リストが作成されるときに指定され、リストの存続期間中は同じままです。</span><span class="sxs-lookup"><span data-stu-id="63d8c-558">The type of the list is specified when the list is created, and remains the same throughout the life of the list.</span></span>

### <a name="method-xml"></a><span data-ttu-id="63d8c-559">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="63d8c-559">Method xml</span></span>

<span data-ttu-id="63d8c-560">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-560">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="63d8c-561">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-561">Parameters</span></span>

<span data-ttu-id="63d8c-562">インデント</span><span class="sxs-lookup"><span data-stu-id="63d8c-562">indent</span></span>  
<span data-ttu-id="63d8c-563">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="63d8c-563">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-564">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-564">Return Value</span></span>

<span data-ttu-id="63d8c-565">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-565">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-566">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-566">Remarks</span></span>

<span data-ttu-id="63d8c-567">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-567">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-create"></a><span data-ttu-id="63d8c-568">メソッド create</span><span class="sxs-lookup"><span data-stu-id="63d8c-568">Method create</span></span>

<span data-ttu-id="63d8c-569">以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-569">Creates a list from the container obtained from a prior call to the List.pack method.</span></span>

    public static List create(container container)

#### <a name="parameters"></a><span data-ttu-id="63d8c-570">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-570">Parameters</span></span>

<span data-ttu-id="63d8c-571">コンテナー</span><span class="sxs-lookup"><span data-stu-id="63d8c-571">container</span></span>  
<span data-ttu-id="63d8c-572">パックされたリストを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="63d8c-572">The container that holds the packed list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-573">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-573">Return Value</span></span>

<span data-ttu-id="63d8c-574">コンテナーに梱包されたものと同一のリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-574">A list identical to the one that was packed into the container.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-575">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-575">Examples</span></span>

<span data-ttu-id="63d8c-576">次の例では、リストを作成し、それをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-576">The following example creates a list and packs it into a container.</span></span> <span data-ttu-id="63d8c-577">次に、create メソッドを使用してコンテナーを展開し、元のリストと同じリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-577">The create method is then used to unpack the container and create a list identical to the original one.</span></span>

    { 
        List il = new List(Types::Integer); 
        List newList; 
        container packedList; 
        // Add some elements 
        il.addEnd(1); 
        il.addEnd(2); 
        il.addEnd(3); 
        // Pack the list into a container 
        packedList = il.pack(); 
        newList = list::create(packedList); 
        // Prints <1, 2, 3> 
        print newList.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a><span data-ttu-id="63d8c-578">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="63d8c-578">Method createFromXML</span></span>

    public static List createFromXML(Object xmlnode)

#### <a name="parameters"></a><span data-ttu-id="63d8c-579">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-579">Parameters</span></span>

<span data-ttu-id="63d8c-580">xmlnode</span><span class="sxs-lookup"><span data-stu-id="63d8c-580">xmlnode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-581">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-581">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="63d8c-582">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="63d8c-582">Method equal</span></span>

<span data-ttu-id="63d8c-583">2 つのリストが同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-583">Determines whether two lists are identical.</span></span>

    public static boolean equal(List list1, List list2)

#### <a name="parameters"></a><span data-ttu-id="63d8c-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-584">Parameters</span></span>

<span data-ttu-id="63d8c-585">list1</span><span class="sxs-lookup"><span data-stu-id="63d8c-585">list1</span></span>  
<span data-ttu-id="63d8c-586">比較する 2 番目のリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-586">The second list to be compared.</span></span>

<!-- -->

<span data-ttu-id="63d8c-587">list2</span><span class="sxs-lookup"><span data-stu-id="63d8c-587">list2</span></span>  
<span data-ttu-id="63d8c-588">比較する 2 番目のリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-588">The second list to be compared.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-589">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-589">Return Value</span></span>

<span data-ttu-id="63d8c-590">2 つのリストが同一である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-590">true if the two lists are identical; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-591">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-591">Remarks</span></span>

<span data-ttu-id="63d8c-592">2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-592">A list is equal to another list if the two lists are the same type, contain the same number of elements, and the elements occur in the same order.</span></span>

### <a name="method-merge"></a><span data-ttu-id="63d8c-593">メソッド merge</span><span class="sxs-lookup"><span data-stu-id="63d8c-593">Method merge</span></span>

<span data-ttu-id="63d8c-594">2 つのリストを組み合わせ、新しいリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-594">Combines two lists to create a new list.</span></span>

    public static List merge(List list1, List list2)

#### <a name="parameters"></a><span data-ttu-id="63d8c-595">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-595">Parameters</span></span>

<span data-ttu-id="63d8c-596">list1</span><span class="sxs-lookup"><span data-stu-id="63d8c-596">list1</span></span>  
<span data-ttu-id="63d8c-597">新しいリストを作成するために最初のリストの最後に追加されるリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-597">The list that will be added to the end of the first to create the new list.</span></span>

<!-- -->

<span data-ttu-id="63d8c-598">list2</span><span class="sxs-lookup"><span data-stu-id="63d8c-598">list2</span></span>  
<span data-ttu-id="63d8c-599">新しいリストを作成するために最初のリストの最後に追加されるリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-599">The list that will be added to the end of the first to create the new list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-600">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-600">Return Value</span></span>

<span data-ttu-id="63d8c-601">新しいリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-601">The new list.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-602">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-602">Remarks</span></span>

<span data-ttu-id="63d8c-603">リストのタイプは同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-603">The types of the lists must be the same.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-604">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-604">Examples</span></span>

<span data-ttu-id="63d8c-605">次の例では、2 つの整数値のリストを作成し、それらをマージして新しいリストを作成し、新しい組み合わせリストに値を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-605">The following example creates two lists of integer values, merges them to create a new list, and then prints out the values in the new combined list.</span></span>

    { 
        List list1  = new List(Types::Integer); 
        List list2  = new List(Types::Integer); 
        List combinedList  = new List(Types::Integer); 
        int  i; 
        for(i=1; i<6; i++) 
        { 
            List1.addEnd(i); 
        } 
         for(i=6; i<11; i++) 
        { 
            List2.addEnd(i); 
        } 
        combinedList = List::merge(list1, list2); 
        print combinedList.toString(); 
        pause; 
    }

### <a name="method-appendlist"></a><span data-ttu-id="63d8c-606">メソッド appendList</span><span class="sxs-lookup"><span data-stu-id="63d8c-606">Method appendList</span></span>

    public void appendList(List list)

#### <a name="parameters"></a><span data-ttu-id="63d8c-607">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-607">Parameters</span></span>

<span data-ttu-id="63d8c-608">リスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-608">list</span></span>  

### <a name="method-new"></a><span data-ttu-id="63d8c-609">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-609">Method new</span></span>

<span data-ttu-id="63d8c-610">リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-610">Creates a list.</span></span>

    public void new(Types Type)

#### <a name="parameters"></a><span data-ttu-id="63d8c-611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-611">Parameters</span></span>

<span data-ttu-id="63d8c-612">種類</span><span class="sxs-lookup"><span data-stu-id="63d8c-612">Type</span></span>  
<span data-ttu-id="63d8c-613">リスト内の要素が持つべきタイプ。</span><span class="sxs-lookup"><span data-stu-id="63d8c-613">The type that the elements in the list should have.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-614">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-614">Remarks</span></span>

<span data-ttu-id="63d8c-615">Type パラメーターの使用可能な値は、Type システム列挙によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-615">The possible values for the Type parameter are supplied by the Types system enum.</span></span> <span data-ttu-id="63d8c-616">リストを作成した後、そのリストに含まれている要素のタイプを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="63d8c-616">After you have created a list, you cannot change the type of the elements it contains.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-617">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-617">Examples</span></span>

<span data-ttu-id="63d8c-618">次の例では、文字列のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-618">The following example creates a list of strings.</span></span>

    { 
        // Creates a list of integers. 
        List il = new List(Types::String); 
    }

## <a name="class-listenumerator"></a><span data-ttu-id="63d8c-619">クラス ListEnumerator</span><span class="sxs-lookup"><span data-stu-id="63d8c-619">Class ListEnumerator</span></span>
    class ListEnumerator extends Object

<span data-ttu-id="63d8c-620">ListEnumerator クラスを使用すると、一覧内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-620">The ListEnumerator class lets you traverse the elements in a list.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-621">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-621">Remarks</span></span>

<span data-ttu-id="63d8c-622">リストの列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-622">List enumerators start before the first element in the list.</span></span> <span data-ttu-id="63d8c-623">リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-623">You must call the ListEnumerator.moveNext method to make it point to the first element in the list.</span></span> <span data-ttu-id="63d8c-624">list.getEnumerator メソッドが呼び出されたときに、リストと同じ層で列挙子が自動的に作成されるため、ListIterator クラスではなく、ListEnumerator クラスを使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="63d8c-624">It is best practice to use the ListEnumerator class instead of the ListIterator class, because enumerators are automatically created on the same tier as the list (when the list.getEnumerator method is called).</span></span> <span data-ttu-id="63d8c-625">これにより、Caller from としてマークされたコードの潜在的な問題を回避します。反復子とリストは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-625">This avoids a potential problem in code that is marked as Called from, where the iterator and list can be on separate tiers.</span></span> <span data-ttu-id="63d8c-626">さらに、リスト列挙子はリスト反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-626">In addition, list enumerators require less code than list iterators and therefore perform slightly better.</span></span> <span data-ttu-id="63d8c-627">リスト反復子を使用する必要がある唯一の状況は、リストから項目を削除する場合です (ListIterator.delete メソッドを使用します)。</span><span class="sxs-lookup"><span data-stu-id="63d8c-627">The only situation where you have to use a list iterator is if you want to delete items from a list (use the ListIterator.delete method).</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-628">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-628">Examples</span></span>

<span data-ttu-id="63d8c-629">次の例では、整数のリストを作成し、いくつかの値をその中に入れます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-629">The following example creates a list of integers and puts some values into it.</span></span> <span data-ttu-id="63d8c-630">その後、列挙子を作成し、一覧の最初の要素、一覧の 2 番目の要素に列挙子を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-630">It then creates an enumerator, and then sets the enumerator to the first element in the list and then the second element in the list.</span></span>

    { 
        List list = new List(Types::Integer); 
        ListEnumerator enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Print a description of the list 
        print enumerator.definitionString(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // Print contents of first and second elements 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        enumerator.moveNext(); 
        print enumerator.toString(); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="63d8c-631">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-631">Methods</span></span>

| <span data-ttu-id="63d8c-632">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-632">Method</span></span>                        | <span data-ttu-id="63d8c-633">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-633">Description</span></span>                                                                                                   |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-634">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="63d8c-634">public AnyType current()</span></span>      | <span data-ttu-id="63d8c-635">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-635">Retrieves the value that is pointed to by the enumerator.</span></span>                                                     |
| <span data-ttu-id="63d8c-636">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-636">public str definitionString()</span></span> | <span data-ttu-id="63d8c-637">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-637">Returns a description of the enumerator.</span></span>                                                                      |
| <span data-ttu-id="63d8c-638">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="63d8c-638">public boolean moveNext()</span></span>     | <span data-ttu-id="63d8c-639">列挙子が有効なリスト要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-639">Determines whether the enumerator denotes a valid list element.</span></span>                                               |
| <span data-ttu-id="63d8c-640">public str toString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-640">public str toString()</span></span>         | <span data-ttu-id="63d8c-641">列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-641">Returns a description of the content of the element in the list that the enumerator is currently pointing to.</span></span> |
| <span data-ttu-id="63d8c-642">public void reset()</span><span class="sxs-lookup"><span data-stu-id="63d8c-642">public void reset()</span></span>           | <span data-ttu-id="63d8c-643">列挙子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-643">Moves the enumerator to the start of the list.</span></span>                                                                |

### <a name="method-current"></a><span data-ttu-id="63d8c-644">メソッド current</span><span class="sxs-lookup"><span data-stu-id="63d8c-644">Method current</span></span>

<span data-ttu-id="63d8c-645">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-645">Retrieves the value that is pointed to by the enumerator.</span></span>

    public AnyType current()

#### <a name="return-value"></a><span data-ttu-id="63d8c-646">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-646">Return Value</span></span>

<span data-ttu-id="63d8c-647">リスト内で現在指定されている値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-647">The value that is currently pointed to in the list.</span></span> <span data-ttu-id="63d8c-648">戻り値のタイプは、リスト内の項目のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-648">The type of the return value is determined by the type of the items in the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-649">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-649">Examples</span></span>

<span data-ttu-id="63d8c-650">次の例では、リストを反復処理し、dimensionTopic 変数を現在のリスト要素の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-650">The following example iterates through the list and sets the dimensionTopic variable to the value of the current list element.</span></span>

    public DimensionTopic firstDimensionTopic() 
    { 
        DimensionTopic  dimensionTopic; 
        ListEnumerator  enumerator; 
        enumerator = this.getTopicsEnumerator(); 
        if (enumerator.moveNext()) 
        { 
            dimensionTopic = enumerator.current(); 
        } 
        return dimensionTopic; 
    }

### <a name="method-definitionstring"></a><span data-ttu-id="63d8c-651">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="63d8c-651">Method definitionString</span></span>

<span data-ttu-id="63d8c-652">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-652">Returns a description of the enumerator.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-653">Return Value</span></span>

<span data-ttu-id="63d8c-654">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-654">A string that contains a description of the enumerator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-655">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-655">Remarks</span></span>

<span data-ttu-id="63d8c-656">たとえば、整数のリストの列挙子は、int リスト列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-656">For example, an enumerator for a list of integers would return int list enumerator.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-657">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-657">Examples</span></span>

<span data-ttu-id="63d8c-658">次の例では、リストとそのリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-658">The following example creates a list and an enumerator for the list.</span></span> <span data-ttu-id="63d8c-659">definitionString メソッドを使用して、列挙子の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-659">It uses the definitionString method to print a description of the enumerator.</span></span>

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        ; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        print enumerator.definitionString(); 
        pause; 
    }

### <a name="method-movenext"></a><span data-ttu-id="63d8c-660">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="63d8c-660">Method moveNext</span></span>

<span data-ttu-id="63d8c-661">列挙子が有効なリスト要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-661">Determines whether the enumerator denotes a valid list element.</span></span>

    public boolean moveNext()

#### <a name="return-value"></a><span data-ttu-id="63d8c-662">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-662">Return Value</span></span>

<span data-ttu-id="63d8c-663">リスト内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-663">true if the current position in the list holds a valid element; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-664">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-664">Remarks</span></span>

<span data-ttu-id="63d8c-665">リストの列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-665">List enumerators start before the first element in the list.</span></span> <span data-ttu-id="63d8c-666">リストの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-666">You must call the moveNext method to make it point to the first element in the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-667">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-667">Examples</span></span>

<span data-ttu-id="63d8c-668">次の例では、moveNext メソッドを使用してリスト内に別の要素があるかどうかを確認し、dimensionTopic 変数を現在のリスト要素の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-668">The following example uses the moveNext method to check whether there is another element in the list and then sets the dimensionTopic variable to the value of the current list element.</span></span>

    public DimensionTopic firstDimensionTopic() 
    { 
        DimensionTopic  dimensionTopic; 
        ListEnumerator  enumerator; 
        enumerator = this.getTopicsEnumerator(); 
        if (enumerator.moveNext()) 
        { 
            dimensionTopic = enumerator.current(); 
        } 
        return dimensionTopic; 
    }

### <a name="method-tostring"></a><span data-ttu-id="63d8c-669">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="63d8c-669">Method toString</span></span>

<span data-ttu-id="63d8c-670">列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-670">Returns a description of the content of the element in the list that the enumerator is currently pointing to.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-671">Return Value</span></span>

<span data-ttu-id="63d8c-672">現在のリスト要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-672">A string that contains a description of the current list element.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-673">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-673">Examples</span></span>

<span data-ttu-id="63d8c-674">次の例では、リストを作成し、最初の要素と 2 番目の要素の内容をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-674">The following example creates a list, and then prints the content of the first and second elements in the list.</span></span>

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        pause; 
        enumerator.moveNext(); 
        //Print second element in list (1) 
        print enumerator.toString(); 
        pause; 
    }

### <a name="method-reset"></a><span data-ttu-id="63d8c-675">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="63d8c-675">Method reset</span></span>

<span data-ttu-id="63d8c-676">列挙子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-676">Moves the enumerator to the start of the list.</span></span>

    public void reset()

#### <a name="remarks"></a><span data-ttu-id="63d8c-677">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-677">Remarks</span></span>

<span data-ttu-id="63d8c-678">reset メソッドは、列挙子をリストの先頭、リストの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-678">The reset method moves the enumerator to the start of the list, before the first element in the list.</span></span> <span data-ttu-id="63d8c-679">リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-679">You must call the ListEnumerator.moveNext method to make it point to the first element in the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-680">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-680">Examples</span></span>

<span data-ttu-id="63d8c-681">次の例では、リストを作成し、そのリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-681">The following example creates a list and then an enumerator for the list.</span></span> <span data-ttu-id="63d8c-682">reset メソッドを使用して一覧の先頭に移動し、moveNext メソッドを使用して一覧の最初の要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-682">It uses the reset method to move to the start of the list and then uses the moveNext method to move to the first element in the list.</span></span>

    { 
        List list = new List(Types::Integer); 
        ListEnumerator  enumerator; 
        // Add some elements to the list 
        list.addEnd(1); 
        list.addEnd(2); 
        list.addStart(3); 
        // Set the enumerator 
        enumerator = list.getEnumerator(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        //Go to the first element in the List 
        enumerator.moveNext(); 
        // First element is 3 as this was added to start of list 
        print enumerator.toString(); 
        pause; 
    }

## <a name="class-listiterator"></a><span data-ttu-id="63d8c-683">クラス ListIterator</span><span class="sxs-lookup"><span data-stu-id="63d8c-683">Class ListIterator</span></span>
    class ListIterator extends Object

<span data-ttu-id="63d8c-684">ListIterator クラスは、一覧内の要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-684">The ListIterator class is used to iterate over the elements in a list.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-685">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-685">Remarks</span></span>

<span data-ttu-id="63d8c-686">リストの反復子は、反復処理する対象となるリストにポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-686">List iterators can be viewed as pointers into the lists over which they iterate.</span></span> <span data-ttu-id="63d8c-687">繰り返しを開始する機能は利用可能であり、より多くの要素が利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-687">Functionality is available to start the iteration, determine whether more elements are available, and fetch the element that is pointed to by the iterator.</span></span> <span data-ttu-id="63d8c-688">繰り返し中に要素が発生する順序は、要素が挿入される順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-688">The order in which the elements occur during iteration is defined by the sequence in which the elements are inserted.</span></span> <span data-ttu-id="63d8c-689">要素を挿入するには、List.addStart、List.addEnd、または ListIterator.insert メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-689">Elements can be inserted by using the List.addStart, List.addEnd, or ListIterator.insert method.</span></span> <span data-ttu-id="63d8c-690">ListIterator クラスよりも ListEnumerator クラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-690">It is better to use the ListEnumerator class than the ListIterator class.</span></span> <span data-ttu-id="63d8c-691">反復処理するリストの反復子およびマップは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-691">List iterators and the maps over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="63d8c-692">ListIterator クラスを使用し、コードが Called from としてマークされている場合、リストと反復子が別の層で終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-692">If you use the ListIterator class, and code is marked as Called from, it is possible that the list and the iterator will be on different tiers.</span></span> <span data-ttu-id="63d8c-693">この場合、コードは失敗します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-693">In this case, the code will fail.</span></span> <span data-ttu-id="63d8c-694">ListEnumerator クラスを使用する場合、列挙子はリストと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-694">If you use the ListEnumerator class, the enumerator is automatically created on the same tier as the list.</span></span> <span data-ttu-id="63d8c-695">また、リスト内の次のアイテムに移動するには、反復子リストを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-695">Additionally, to move to the next item in a list, you must explicitly call the more and next methods if you are using a list iterator.</span></span> <span data-ttu-id="63d8c-696">ListEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="63d8c-696">If you use the ListEnumerator class, you only have to call the moveNext method.</span></span> <span data-ttu-id="63d8c-697">リスト列挙子を使用できない唯一の状況は、リストから要素を削除する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-697">The only situation where you cannot use a list enumerator is where you need to delete elements from a list.</span></span> <span data-ttu-id="63d8c-698">詳細については、「メソッドの削除」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63d8c-698">For more information, see the delete method.</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-699">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-699">Examples</span></span>

<span data-ttu-id="63d8c-700">次の例では、リストとそれを指す反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-700">The following example creates a list and an iterator to point to it.</span></span> <span data-ttu-id="63d8c-701">ListIterator クラスのさまざまなメソッドを使用して、一覧の説明と一覧内の項目を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-701">It then uses various methods on the ListIterator class to print a description of the list, and the items in the list.</span></span>

    { 
        List il = new List(types::Integer); 
        ListIterator it; 
        // Add some elements into the list. 
        il.addStart(1); 
        il.addStart(2); 
        il.addStart(4);  
        // Create a list iterator to traverse the values. 
        it = new ListIterator (il);  
        // Prints "int list iterator". 
        print it.definitionString();  
        // Prints "(begin)[4]". 
        print it.toString();  
        // Go on for as long as elements are found in the list. 
        // Prints 4, 2, 1. 
        while (it.more()) 
        { 
            print it.value(); 
            it.next(); 
        } 
        // Prints (end). 
        print it.toString(); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="63d8c-702">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-702">Methods</span></span>

| <span data-ttu-id="63d8c-703">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-703">Method</span></span>                               | <span data-ttu-id="63d8c-704">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-704">Description</span></span>                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-705">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-705">public str definitionString()</span></span>        | <span data-ttu-id="63d8c-706">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-706">Returns a textual representation of the type of the iterator.</span></span>                                  |
| <span data-ttu-id="63d8c-707">public AnyType insert(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="63d8c-707">public AnyType insert(AnyType value)</span></span> | <span data-ttu-id="63d8c-708">反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-708">Inserts a new value at the position in the list that the iterator currently points to.</span></span>         |
| <span data-ttu-id="63d8c-709">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="63d8c-709">public boolean more()</span></span>                | <span data-ttu-id="63d8c-710">リスト反復子が有効な要素を指しているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-710">Determines whether the list iterator points to a valid element.</span></span>                                |
| <span data-ttu-id="63d8c-711">public str toString()</span><span class="sxs-lookup"><span data-stu-id="63d8c-711">public str toString()</span></span>                | <span data-ttu-id="63d8c-712">反復子によりポイントされている現在のリスト値のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-712">Returns a textual representation of the current list value that is pointed to by the iterator.</span></span> |
| <span data-ttu-id="63d8c-713">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="63d8c-713">public AnyType value()</span></span>               | <span data-ttu-id="63d8c-714">反復子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-714">Retrieves the value that is pointed to by the iterator.</span></span>                                        |
| <span data-ttu-id="63d8c-715">public void begin()</span><span class="sxs-lookup"><span data-stu-id="63d8c-715">public void begin()</span></span>                  | <span data-ttu-id="63d8c-716">反復子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-716">Moves the iterator to the start of the list.</span></span>                                                   |
| <span data-ttu-id="63d8c-717">public void next()</span><span class="sxs-lookup"><span data-stu-id="63d8c-717">public void next()</span></span>                   | <span data-ttu-id="63d8c-718">リストで次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-718">Moves the iterator to the next element in the list.</span></span>                                            |
| <span data-ttu-id="63d8c-719">public void end()</span><span class="sxs-lookup"><span data-stu-id="63d8c-719">public void end()</span></span>                    | <span data-ttu-id="63d8c-720">リストで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-720">Moves the iterator past the last element in the list.</span></span>                                          |
| <span data-ttu-id="63d8c-721">public void delete()</span><span class="sxs-lookup"><span data-stu-id="63d8c-721">public void delete()</span></span>                 | <span data-ttu-id="63d8c-722">反復子によってポイントされている要素を一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-722">Removes the element that is pointed to by the iterator from the list.</span></span>                          |
| <span data-ttu-id="63d8c-723">public void new(List list)</span><span class="sxs-lookup"><span data-stu-id="63d8c-723">public void new(List list)</span></span>           | <span data-ttu-id="63d8c-724">特定のリストに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-724">Creates a new iterator for a particular list.</span></span>                                                  |

### <a name="method-definitionstring"></a><span data-ttu-id="63d8c-725">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="63d8c-725">Method definitionString</span></span>

<span data-ttu-id="63d8c-726">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-726">Returns a textual representation of the type of the iterator.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-727">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-727">Return Value</span></span>

<span data-ttu-id="63d8c-728">反復子のタイプを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-728">A string that contains the type of the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-729">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-729">Remarks</span></span>

<span data-ttu-id="63d8c-730">例: int リスト反復子。</span><span class="sxs-lookup"><span data-stu-id="63d8c-730">For example: int list iterator.</span></span>

### <a name="method-insert"></a><span data-ttu-id="63d8c-731">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="63d8c-731">Method insert</span></span>

<span data-ttu-id="63d8c-732">反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-732">Inserts a new value at the position in the list that the iterator currently points to.</span></span>

    public AnyType insert(AnyType value)

#### <a name="parameters"></a><span data-ttu-id="63d8c-733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-733">Parameters</span></span>

<span data-ttu-id="63d8c-734">値</span><span class="sxs-lookup"><span data-stu-id="63d8c-734">value</span></span>  
<span data-ttu-id="63d8c-735">リストに挿入する項目の値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-735">The value of the item to insert into the list.</span></span>

#### <a name="return-value"></a><span data-ttu-id="63d8c-736">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-736">Return Value</span></span>

<span data-ttu-id="63d8c-737">リストに挿入された値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-737">The value that was inserted into the list.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-738">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-738">Remarks</span></span>

<span data-ttu-id="63d8c-739">value パラメーターは、リストと同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-739">The value parameter must be the same type as the list.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-740">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-740">Examples</span></span>

<span data-ttu-id="63d8c-741">次の例では、10 個のアイテムを持つリストを作成し、ListIterator.insert メソッドを使用してリスト内の 3 番目のアイテムとして新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-741">The following example creates a list that has ten items and then uses the ListIterator.insert method to insert a new value as the third item in the list.</span></span>

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        int j = 25; 
        // Insert values 1 to 10 into the list 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Go to the 3rd element in the list 
        it = new ListIterator(il); 
        it.begin(); 
        it.next(); 
        it.next(); 
        // Insert a new value (25) 
        it.insert(j); 
      it.begin(); 
        // Print all values in the list. 
        // 25 is the third value in the list 
        while (it.more()) 
        { 
            print it.value(); 
            it.next();  
        } 
        pause; 
    }

### <a name="method-more"></a><span data-ttu-id="63d8c-742">メソッド more</span><span class="sxs-lookup"><span data-stu-id="63d8c-742">Method more</span></span>

<span data-ttu-id="63d8c-743">リスト反復子が有効な要素を指しているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-743">Determines whether the list iterator points to a valid element.</span></span>

    public boolean more()

#### <a name="return-value"></a><span data-ttu-id="63d8c-744">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-744">Return Value</span></span>

<span data-ttu-id="63d8c-745">リスト反復子が有効な要素を指定する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-745">true if the list iterator points to a valid element; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-746">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-746">Remarks</span></span>

<span data-ttu-id="63d8c-747">このメソッドが false を返すときに要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-747">Attempting to access an element when this method returns false will cause an error.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-748">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-748">Examples</span></span>

<span data-ttu-id="63d8c-749">次の例では、ListIterator.more メソッドを使用してリストに要素があるかどうかを確認し、リスト内のすべての要素の値を出力する while ループを実行します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-749">The following example uses the ListIterator.more method to check whether there are more elements in the list and then runs through the while loop, which prints the values of all the elements in the list.</span></span>

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        // Add some elements 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Traverse the list 
        it = new ListIterator(il); 
        while (it.more()) 
        { 
            print it.value(); 
            it.next(); // Skip to the next element 
        } 
        pause; 
    }

### <a name="method-tostring"></a><span data-ttu-id="63d8c-750">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="63d8c-750">Method toString</span></span>

<span data-ttu-id="63d8c-751">反復子によりポイントされている現在のリスト値のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-751">Returns a textual representation of the current list value that is pointed to by the iterator.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="63d8c-752">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-752">Return Value</span></span>

<span data-ttu-id="63d8c-753">現在の値の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="63d8c-753">A string that contains a description of the current value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-754">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-754">Remarks</span></span>

<span data-ttu-id="63d8c-755">反復子がリスト内の最初の要素を指している場合、文字列には "(開始)\[値\]" という形式の文字列が含まれます。反復子が要素を指していない場合 (つまり、more() メソッドが false を返す場合)、返される次の文字列は: (終了) になります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-755">If the iterator points to the first element in the list, the string will contain an indication of this, in the form "(begin)\[value\]" If the iterator does not point to an element (that is, the more() method returns false), the following string returned is: (end).</span></span> <span data-ttu-id="63d8c-756">反復子が値をポイントしている場合、文字列は "\[値\]" で、値が要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-756">If the iterator points to a value, the string is "\[value\]", where value is a string representation of the element value.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-757">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-757">Examples</span></span>

<span data-ttu-id="63d8c-758">次の例では、リスト内の 2 つの値の値の説明を表示します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-758">The following example prints the following description of the values of the two values in a list:</span></span>

1.  <span data-ttu-id="63d8c-759">(開始) \[2\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-759">(begin) \[2\]</span></span>
2.  <span data-ttu-id="63d8c-760">\[1\]</span><span class="sxs-lookup"><span data-stu-id="63d8c-760">\[1\]</span></span>

<!-- -->

    { 
        List li = new List(Types::Integer); 
        ListIterator it = new ListIterator(li); 
        li.addStart(1); 
        li.addStart(2); // This is now the first value 
        it.begin(); 
        print it.toString(); 
        it.next(); 
        print it.toString(); 
        pause; 
    }

### <a name="method-value"></a><span data-ttu-id="63d8c-761">メソッド value</span><span class="sxs-lookup"><span data-stu-id="63d8c-761">Method value</span></span>

<span data-ttu-id="63d8c-762">反復子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-762">Retrieves the value that is pointed to by the iterator.</span></span>

    public AnyType value()

#### <a name="return-value"></a><span data-ttu-id="63d8c-763">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-763">Return Value</span></span>

<span data-ttu-id="63d8c-764">反復子によりポイントされている値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-764">The value that is pointed to by the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-765">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-765">Remarks</span></span>

<span data-ttu-id="63d8c-766">リスト要素の値を取得する前に、ListIterator.more メソッドを使用して要素が存在するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-766">Before you try to retrieve the value of a list element, use the ListIterator.more method to test whether an element exists.</span></span>

### <a name="method-begin"></a><span data-ttu-id="63d8c-767">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="63d8c-767">Method begin</span></span>

<span data-ttu-id="63d8c-768">反復子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-768">Moves the iterator to the start of the list.</span></span>

    public void begin()

### <a name="method-next"></a><span data-ttu-id="63d8c-769">メソッド next</span><span class="sxs-lookup"><span data-stu-id="63d8c-769">Method next</span></span>

<span data-ttu-id="63d8c-770">リストで次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-770">Moves the iterator to the next element in the list.</span></span>

    public void next()

#### <a name="remarks"></a><span data-ttu-id="63d8c-771">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-771">Remarks</span></span>

<span data-ttu-id="63d8c-772">ListIterator.more メソッドを使用して、反復子が有効な要素を指しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-772">Use the ListIterator.more method to determine whether the iterator points to a valid element.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-773">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-773">Examples</span></span>

<span data-ttu-id="63d8c-774">次の例では、ListIterator.next メソッドを使用して、各要素の値が出力されるときにリストをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="63d8c-774">The following example uses the ListIterator.next method to traverse a list as the value of each element is printed.</span></span>

    { 
        List il = new List(Types::Integer); 
        ListIterator it; 
        int i; 
        // Add some elements 
        for (i = 1; i <= 10; i++) 
        { 
            il.addEnd(i); 
        } 
        // Traverse the list 
        it = new ListIterator(il); 
        while (it.more()) 
        { 
            print it.value(); 
            // Move to the next element 
            it.next();  
        } 
        pause; 
    }

### <a name="method-end"></a><span data-ttu-id="63d8c-775">メソッド end</span><span class="sxs-lookup"><span data-stu-id="63d8c-775">Method end</span></span>

<span data-ttu-id="63d8c-776">リストで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-776">Moves the iterator past the last element in the list.</span></span>

    public void end()

#### <a name="remarks"></a><span data-ttu-id="63d8c-777">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-777">Remarks</span></span>

<span data-ttu-id="63d8c-778">このメソッドが実行すると、ListIterator.more メソッドが false に戻ります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-778">After this method runs, the ListIterator.more method will return false.</span></span>

### <a name="method-delete"></a><span data-ttu-id="63d8c-779">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="63d8c-779">Method delete</span></span>

<span data-ttu-id="63d8c-780">反復子によってポイントされている要素を一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-780">Removes the element that is pointed to by the iterator from the list.</span></span>

    public void delete()

#### <a name="remarks"></a><span data-ttu-id="63d8c-781">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-781">Remarks</span></span>

<span data-ttu-id="63d8c-782">反復子は、この削除の後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-782">The iterator will point to the next element after the deletion.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-783">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-783">Examples</span></span>

<span data-ttu-id="63d8c-784">次の例では、3 つの要素を含むリストを作成し、リスト内の要素の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-784">The following example creates a list that contains three elements and prints a description of the elements in the list.</span></span> <span data-ttu-id="63d8c-785">一覧の最初の要素を削除し、残りの要素の説明を印刷します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-785">It then deletes the first element in the list and prints a description of the remaining elements.</span></span>

    { 
        List li = new List(Types::Integer); 
        ListIterator it; 
        li.addStart(1); 
        li.addStart(2); 
        li.addStart(3); 
        print li.toString(); 
        it = new ListIterator(li); 
        it.delete(); 
        print li.toString(); 
        pause; 
    }

### <a name="method-new"></a><span data-ttu-id="63d8c-786">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-786">Method new</span></span>

<span data-ttu-id="63d8c-787">特定のリストに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-787">Creates a new iterator for a particular list.</span></span>

    public void new(List list)

#### <a name="parameters"></a><span data-ttu-id="63d8c-788">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-788">Parameters</span></span>

<span data-ttu-id="63d8c-789">リスト</span><span class="sxs-lookup"><span data-stu-id="63d8c-789">list</span></span>  
<span data-ttu-id="63d8c-790">反復子を作成するリスト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-790">The list for which to create an iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-791">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-791">Remarks</span></span>

<span data-ttu-id="63d8c-792">反復子は、リストが空でない場合、リストの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-792">The iterator is positioned at the first value in the list, if the list is not empty.</span></span> <span data-ttu-id="63d8c-793">反復子および繰り返すリストは、同じクライアント/サーバー側にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-793">Iterators and the lists that they iterate over must be on the same client/server side.</span></span>

#### <a name="examples"></a><span data-ttu-id="63d8c-794">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-794">Examples</span></span>

<span data-ttu-id="63d8c-795">次の例では、整数リストの反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-795">The following example creates an iterator for a list of integers.</span></span>

    List il = new List(types::Integer); 
    ListIterator it; 
    it = new ListIterator (il);

## <a name="class-listpage"></a><span data-ttu-id="63d8c-796">クラス ListPage</span><span class="sxs-lookup"><span data-stu-id="63d8c-796">Class ListPage</span></span>
    class ListPage extends Page

### <a name="remarks"></a><span data-ttu-id="63d8c-797">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-797">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-798">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-798">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-799">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-799">Methods</span></span>

| <span data-ttu-id="63d8c-800">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-800">Method</span></span>                                                                      | <span data-ttu-id="63d8c-801">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-801">Description</span></span>                                       |
|-----------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="63d8c-802">public str actionPaneControlParameters(str controlName, \[str parameters\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-802">public str actionPaneControlParameters(str controlName, \[str parameters\])</span></span> |                                                   |
| <span data-ttu-id="63d8c-803">public Array activeActionPaneTabNames()</span><span class="sxs-lookup"><span data-stu-id="63d8c-803">public Array activeActionPaneTabNames()</span></span>                                     | <span data-ttu-id="63d8c-804">指定された有効なタブの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-804">Gets the name of the specified active tab.</span></span>        |
| <span data-ttu-id="63d8c-805">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-805">public str caption(\[str value\])</span></span>                                           |                                                   |
| <span data-ttu-id="63d8c-806">public ListPageArgs listPageArgs()</span><span class="sxs-lookup"><span data-stu-id="63d8c-806">public ListPageArgs listPageArgs()</span></span>                                          |                                                   |
| <span data-ttu-id="63d8c-807">public int listPageFieldDataField(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="63d8c-807">public int listPageFieldDataField(str fieldName)</span></span>                            |                                                   |
| <span data-ttu-id="63d8c-808">public Array listPageFieldNames()</span><span class="sxs-lookup"><span data-stu-id="63d8c-808">public Array listPageFieldNames()</span></span>                                           |                                                   |
| <span data-ttu-id="63d8c-809">public int listPageFieldTableId(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="63d8c-809">public int listPageFieldTableId(str fieldName)</span></span>                              |                                                   |
| <span data-ttu-id="63d8c-810">public boolean listPageFieldVisible(str fieldName, \[boolean visible\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-810">public boolean listPageFieldVisible(str fieldName, \[boolean visible\])</span></span>     |                                                   |
| <span data-ttu-id="63d8c-811">public str modeledQueryName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-811">public str modeledQueryName(\[str value\])</span></span>                                  |                                                   |
| <span data-ttu-id="63d8c-812">public void new()</span><span class="sxs-lookup"><span data-stu-id="63d8c-812">public void new()</span></span>                                                           | <span data-ttu-id="63d8c-813">ListPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-813">Initializes a new instance of the ListPage class.</span></span> |

### <a name="method-actionpanecontrolparameters"></a><span data-ttu-id="63d8c-814">メソッド actionPaneControlParameters</span><span class="sxs-lookup"><span data-stu-id="63d8c-814">Method actionPaneControlParameters</span></span>

    public str actionPaneControlParameters(str controlName, [str parameters])

#### <a name="parameters"></a><span data-ttu-id="63d8c-815">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-815">Parameters</span></span>

<span data-ttu-id="63d8c-816">controlName</span><span class="sxs-lookup"><span data-stu-id="63d8c-816">controlName</span></span>  

<!-- -->

<span data-ttu-id="63d8c-817">パラメータ</span><span class="sxs-lookup"><span data-stu-id="63d8c-817">parameters</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-818">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-818">Return Value</span></span>

### <a name="method-activeactionpanetabnames"></a><span data-ttu-id="63d8c-819">メソッド activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="63d8c-819">Method activeActionPaneTabNames</span></span>

<span data-ttu-id="63d8c-820">指定された有効なタブの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-820">Gets the name of the specified active tab.</span></span>

    public Array activeActionPaneTabNames()

#### <a name="return-value"></a><span data-ttu-id="63d8c-821">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-821">Return Value</span></span>

<span data-ttu-id="63d8c-822">アクティブなタブの名前を含む配列です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-822">An array that contains the names of the active tabs.</span></span>

### <a name="method-caption"></a><span data-ttu-id="63d8c-823">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="63d8c-823">Method caption</span></span>

    public str caption([str value])

#### <a name="parameters"></a><span data-ttu-id="63d8c-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-824">Parameters</span></span>

<span data-ttu-id="63d8c-825">値</span><span class="sxs-lookup"><span data-stu-id="63d8c-825">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-826">Return Value</span></span>

### <a name="method-listpageargs"></a><span data-ttu-id="63d8c-827">メソッド listPageArgs</span><span class="sxs-lookup"><span data-stu-id="63d8c-827">Method listPageArgs</span></span>

    public ListPageArgs listPageArgs()

#### <a name="return-value"></a><span data-ttu-id="63d8c-828">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-828">Return Value</span></span>

### <a name="method-listpagefielddatafield"></a><span data-ttu-id="63d8c-829">メソッド listPageFieldDataField</span><span class="sxs-lookup"><span data-stu-id="63d8c-829">Method listPageFieldDataField</span></span>

    public int listPageFieldDataField(str fieldName)

#### <a name="parameters"></a><span data-ttu-id="63d8c-830">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-830">Parameters</span></span>

<span data-ttu-id="63d8c-831">fieldName</span><span class="sxs-lookup"><span data-stu-id="63d8c-831">fieldName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-832">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-832">Return Value</span></span>

### <a name="method-listpagefieldnames"></a><span data-ttu-id="63d8c-833">メソッド listPageFieldNames</span><span class="sxs-lookup"><span data-stu-id="63d8c-833">Method listPageFieldNames</span></span>

    public Array listPageFieldNames()

#### <a name="return-value"></a><span data-ttu-id="63d8c-834">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-834">Return Value</span></span>

### <a name="method-listpagefieldtableid"></a><span data-ttu-id="63d8c-835">メソッド listPageFieldTableId</span><span class="sxs-lookup"><span data-stu-id="63d8c-835">Method listPageFieldTableId</span></span>

    public int listPageFieldTableId(str fieldName)

#### <a name="parameters"></a><span data-ttu-id="63d8c-836">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-836">Parameters</span></span>

<span data-ttu-id="63d8c-837">fieldName</span><span class="sxs-lookup"><span data-stu-id="63d8c-837">fieldName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-838">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-838">Return Value</span></span>

### <a name="method-listpagefieldvisible"></a><span data-ttu-id="63d8c-839">メソッド listPageFieldVisible</span><span class="sxs-lookup"><span data-stu-id="63d8c-839">Method listPageFieldVisible</span></span>

    public boolean listPageFieldVisible(str fieldName, [boolean visible])

#### <a name="parameters"></a><span data-ttu-id="63d8c-840">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-840">Parameters</span></span>

<span data-ttu-id="63d8c-841">fieldName</span><span class="sxs-lookup"><span data-stu-id="63d8c-841">fieldName</span></span>  

<!-- -->

<span data-ttu-id="63d8c-842">表示</span><span class="sxs-lookup"><span data-stu-id="63d8c-842">visible</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-843">Return Value</span></span>

### <a name="method-modeledqueryname"></a><span data-ttu-id="63d8c-844">メソッド modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="63d8c-844">Method modeledQueryName</span></span>

    public str modeledQueryName([str value])

#### <a name="parameters"></a><span data-ttu-id="63d8c-845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-845">Parameters</span></span>

<span data-ttu-id="63d8c-846">値</span><span class="sxs-lookup"><span data-stu-id="63d8c-846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-847">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="63d8c-848">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-848">Method new</span></span>

<span data-ttu-id="63d8c-849">ListPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-849">Initializes a new instance of the ListPage class.</span></span>

    public void new()

## <a name="class-listpageargs"></a><span data-ttu-id="63d8c-850">クラス ListPageArgs</span><span class="sxs-lookup"><span data-stu-id="63d8c-850">Class ListPageArgs</span></span>
    class ListPageArgs extends PageArgs

### <a name="remarks"></a><span data-ttu-id="63d8c-851">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-851">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-852">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-852">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-853">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-853">Methods</span></span>

| <span data-ttu-id="63d8c-854">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-854">Method</span></span> | <span data-ttu-id="63d8c-855">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-855">Description</span></span> |
|--------|-------------|
|        |             |

## <a name="class-listpageinteraction"></a><span data-ttu-id="63d8c-856">クラス ListPageInteraction</span><span class="sxs-lookup"><span data-stu-id="63d8c-856">Class ListPageInteraction</span></span>
    class ListPageInteraction extends PageInteraction

### <a name="remarks"></a><span data-ttu-id="63d8c-857">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-857">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-858">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-858">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-859">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-859">Methods</span></span>

| <span data-ttu-id="63d8c-860">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-860">Method</span></span>                                           | <span data-ttu-id="63d8c-861">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-861">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="63d8c-862">public ListPage listPage()</span><span class="sxs-lookup"><span data-stu-id="63d8c-862">public ListPage listPage()</span></span>                       |                                                               |
| <span data-ttu-id="63d8c-863">public void tabChanged(container activeTabNames)</span><span class="sxs-lookup"><span data-stu-id="63d8c-863">public void tabChanged(container activeTabNames)</span></span> | <span data-ttu-id="63d8c-864">アクティブなタブが変更されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-864">Called when the active tab is changed.</span></span>                        |
| <span data-ttu-id="63d8c-865">public void initializing()</span><span class="sxs-lookup"><span data-stu-id="63d8c-865">public void initializing()</span></span>                       |                                                               |
| <span data-ttu-id="63d8c-866">public void initialized()</span><span class="sxs-lookup"><span data-stu-id="63d8c-866">public void initialized()</span></span>                        |                                                               |
| <span data-ttu-id="63d8c-867">public void selectionChanged()</span><span class="sxs-lookup"><span data-stu-id="63d8c-867">public void selectionChanged()</span></span>                   |                                                               |
| <span data-ttu-id="63d8c-868">public void initializeQuery(Query query)</span><span class="sxs-lookup"><span data-stu-id="63d8c-868">public void initializeQuery(Query query)</span></span>         |                                                               |
| <span data-ttu-id="63d8c-869">public void new(ListPage listPage)</span><span class="sxs-lookup"><span data-stu-id="63d8c-869">public void new(ListPage listPage)</span></span>               | <span data-ttu-id="63d8c-870">listPage 上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-870">Creates a new PageInteraction object operating on a listPage.</span></span> |

### <a name="method-listpage"></a><span data-ttu-id="63d8c-871">メソッド listPage</span><span class="sxs-lookup"><span data-stu-id="63d8c-871">Method listPage</span></span>

    public ListPage listPage()

#### <a name="return-value"></a><span data-ttu-id="63d8c-872">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-872">Return Value</span></span>

### <a name="method-tabchanged"></a><span data-ttu-id="63d8c-873">メソッド tabChanged</span><span class="sxs-lookup"><span data-stu-id="63d8c-873">Method tabChanged</span></span>

<span data-ttu-id="63d8c-874">アクティブなタブが変更されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-874">Called when the active tab is changed.</span></span>

    public void tabChanged(container activeTabNames)

#### <a name="parameters"></a><span data-ttu-id="63d8c-875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-875">Parameters</span></span>

<span data-ttu-id="63d8c-876">activeTabNames</span><span class="sxs-lookup"><span data-stu-id="63d8c-876">activeTabNames</span></span>  
<span data-ttu-id="63d8c-877">アクティブなタブの名前を含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="63d8c-877">A container containing the names of the active tabs.</span></span>

### <a name="method-initializing"></a><span data-ttu-id="63d8c-878">メソッド initializing</span><span class="sxs-lookup"><span data-stu-id="63d8c-878">Method initializing</span></span>

    public void initializing()

### <a name="method-initialized"></a><span data-ttu-id="63d8c-879">メソッド initialized</span><span class="sxs-lookup"><span data-stu-id="63d8c-879">Method initialized</span></span>

    public void initialized()

### <a name="method-selectionchanged"></a><span data-ttu-id="63d8c-880">メソッド selectionChanged</span><span class="sxs-lookup"><span data-stu-id="63d8c-880">Method selectionChanged</span></span>

    public void selectionChanged()

### <a name="method-initializequery"></a><span data-ttu-id="63d8c-881">メソッド initializeQuery</span><span class="sxs-lookup"><span data-stu-id="63d8c-881">Method initializeQuery</span></span>

    public void initializeQuery(Query query)

#### <a name="parameters"></a><span data-ttu-id="63d8c-882">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-882">Parameters</span></span>

<span data-ttu-id="63d8c-883">クエリ</span><span class="sxs-lookup"><span data-stu-id="63d8c-883">query</span></span>  

### <a name="method-new"></a><span data-ttu-id="63d8c-884">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-884">Method new</span></span>

<span data-ttu-id="63d8c-885">listPage 上で動作する新しい PageInteraction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-885">Creates a new PageInteraction object operating on a listPage.</span></span>

    public void new(ListPage listPage)

#### <a name="parameters"></a><span data-ttu-id="63d8c-886">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-886">Parameters</span></span>

<span data-ttu-id="63d8c-887">listPage</span><span class="sxs-lookup"><span data-stu-id="63d8c-887">listPage</span></span>  
<span data-ttu-id="63d8c-888">指定した ListPage オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="63d8c-888">The specified ListPage object.</span></span>

## <a name="class-loadautocompletedataeventargs"></a><span data-ttu-id="63d8c-889">クラス LoadAutoCompleteDataEventArgs</span><span class="sxs-lookup"><span data-stu-id="63d8c-889">Class LoadAutoCompleteDataEventArgs</span></span>
    class LoadAutoCompleteDataEventArgs extends Object

### <a name="remarks"></a><span data-ttu-id="63d8c-890">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-890">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-891">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-891">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-892">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-892">Methods</span></span>

| <span data-ttu-id="63d8c-893">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-893">Method</span></span>                                                                                          | <span data-ttu-id="63d8c-894">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-894">Description</span></span> |
|-------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="63d8c-895">public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-895">public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\])</span></span> |             |
| <span data-ttu-id="63d8c-896">public boolean canPage(\[boolean canPage\])</span><span class="sxs-lookup"><span data-stu-id="63d8c-896">public boolean canPage(\[boolean canPage\])</span></span>                                                     |             |
| <span data-ttu-id="63d8c-897">public str filterValue()</span><span class="sxs-lookup"><span data-stu-id="63d8c-897">public str filterValue()</span></span>                                                                        |             |
| <span data-ttu-id="63d8c-898">public AnyType lastPagedTag()</span><span class="sxs-lookup"><span data-stu-id="63d8c-898">public AnyType lastPagedTag()</span></span>                                                                   |             |
| <span data-ttu-id="63d8c-899">public FormSegment segment()</span><span class="sxs-lookup"><span data-stu-id="63d8c-899">public FormSegment segment()</span></span>                                                                    |             |
| <span data-ttu-id="63d8c-900">public void addAutoCompleteData(str value, str description, AnyType tag)</span><span class="sxs-lookup"><span data-stu-id="63d8c-900">public void addAutoCompleteData(str value, str description, AnyType tag)</span></span>                        |             |

### <a name="method-autocompletedatamode"></a><span data-ttu-id="63d8c-901">メソッド autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="63d8c-901">Method autoCompleteDataMode</span></span>

    public AutoCompleteDataMode autoCompleteDataMode([AutoCompleteDataMode autoCompleteDataMode])

#### <a name="parameters"></a><span data-ttu-id="63d8c-902">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-902">Parameters</span></span>

<span data-ttu-id="63d8c-903">autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="63d8c-903">autoCompleteDataMode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-904">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-904">Return Value</span></span>

### <a name="method-canpage"></a><span data-ttu-id="63d8c-905">メソッド canPage</span><span class="sxs-lookup"><span data-stu-id="63d8c-905">Method canPage</span></span>

    public boolean canPage([boolean canPage])

#### <a name="parameters"></a><span data-ttu-id="63d8c-906">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-906">Parameters</span></span>

<span data-ttu-id="63d8c-907">canPage</span><span class="sxs-lookup"><span data-stu-id="63d8c-907">canPage</span></span>  

#### <a name="return-value"></a><span data-ttu-id="63d8c-908">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-908">Return Value</span></span>

### <a name="method-filtervalue"></a><span data-ttu-id="63d8c-909">メソッド filterValue</span><span class="sxs-lookup"><span data-stu-id="63d8c-909">Method filterValue</span></span>

    public str filterValue()

#### <a name="return-value"></a><span data-ttu-id="63d8c-910">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-910">Return Value</span></span>

### <a name="method-lastpagedtag"></a><span data-ttu-id="63d8c-911">メソッド lastPagedTag</span><span class="sxs-lookup"><span data-stu-id="63d8c-911">Method lastPagedTag</span></span>

    public AnyType lastPagedTag()

#### <a name="return-value"></a><span data-ttu-id="63d8c-912">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-912">Return Value</span></span>

### <a name="method-segment"></a><span data-ttu-id="63d8c-913">メソッド segment</span><span class="sxs-lookup"><span data-stu-id="63d8c-913">Method segment</span></span>

    public FormSegment segment()

#### <a name="return-value"></a><span data-ttu-id="63d8c-914">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-914">Return Value</span></span>

### <a name="method-addautocompletedata"></a><span data-ttu-id="63d8c-915">メソッド addAutoCompleteData</span><span class="sxs-lookup"><span data-stu-id="63d8c-915">Method addAutoCompleteData</span></span>

    public void addAutoCompleteData(str value, str description, AnyType tag)

#### <a name="parameters"></a><span data-ttu-id="63d8c-916">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-916">Parameters</span></span>

<span data-ttu-id="63d8c-917">値</span><span class="sxs-lookup"><span data-stu-id="63d8c-917">value</span></span>  

<!-- -->

<span data-ttu-id="63d8c-918">description</span><span class="sxs-lookup"><span data-stu-id="63d8c-918">description</span></span>  

<!-- -->

<span data-ttu-id="63d8c-919">タグ</span><span class="sxs-lookup"><span data-stu-id="63d8c-919">tag</span></span>  

## <a name="class-loginproperty"></a><span data-ttu-id="63d8c-920">クラス LoginProperty</span><span class="sxs-lookup"><span data-stu-id="63d8c-920">Class LoginProperty</span></span>
    class LoginProperty extends Object

<span data-ttu-id="63d8c-921">LoginProperty クラスでは、OdbcConnection クラスのインスタンスにログオン情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-921">The LoginProperty class enables logon information to be passed to an instance of the OdbcConnection class.</span></span>

### <a name="remarks"></a><span data-ttu-id="63d8c-922">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-922">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="63d8c-923">例</span><span class="sxs-lookup"><span data-stu-id="63d8c-923">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="63d8c-924">メソッド</span><span class="sxs-lookup"><span data-stu-id="63d8c-924">Methods</span></span>

| <span data-ttu-id="63d8c-925">方法</span><span class="sxs-lookup"><span data-stu-id="63d8c-925">Method</span></span>                                                | <span data-ttu-id="63d8c-926">説明</span><span class="sxs-lookup"><span data-stu-id="63d8c-926">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8c-927">public str getDatabase()</span><span class="sxs-lookup"><span data-stu-id="63d8c-927">public str getDatabase()</span></span>                              | <span data-ttu-id="63d8c-928">LoginProperty クラスに格納されている、データベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-928">Retrieves the name of the database, as stored in the LoginProperty class.</span></span>                                                                                                                              |
| <span data-ttu-id="63d8c-929">public str getDSN()</span><span class="sxs-lookup"><span data-stu-id="63d8c-929">public str getDSN()</span></span>                                   | <span data-ttu-id="63d8c-930">LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-930">Retrieves the data source name (DSN) that is stored in the LoginProperty class.</span></span>                                                                                                                        |
| <span data-ttu-id="63d8c-931">public str getOciServiceName()</span><span class="sxs-lookup"><span data-stu-id="63d8c-931">public str getOciServiceName()</span></span>                        | <span data-ttu-id="63d8c-932">LoginProperty クラスに格納されている Oracle サービス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-932">Retrieves the Oracle service name that is stored in the LoginProperty class.</span></span>                                                                                                                           |
| <span data-ttu-id="63d8c-933">public str getOther()</span><span class="sxs-lookup"><span data-stu-id="63d8c-933">public str getOther()</span></span>                                 | <span data-ttu-id="63d8c-934">LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-934">Retrieves the additional logon parameters that are stored in the LoginProperty class.</span></span>                                                                                                                  |
| <span data-ttu-id="63d8c-935">public str getServer()</span><span class="sxs-lookup"><span data-stu-id="63d8c-935">public str getServer()</span></span>                                | <span data-ttu-id="63d8c-936">LoginProperty クラスに格納されているサーバー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-936">Retrieves the server name that is stored in the LoginProperty class.</span></span>                                                                                                                                   |
| <span data-ttu-id="63d8c-937">public str getTcpIpPort()</span><span class="sxs-lookup"><span data-stu-id="63d8c-937">public str getTcpIpPort()</span></span>                             | <span data-ttu-id="63d8c-938">LoginProperty クラスに格納されている TCP/IP ポートを取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-938">Retrieves the TCP/IP port that is stored in the LoginProperty class.</span></span>                                                                                                                                   |
| <span data-ttu-id="63d8c-939">public boolean getUsePredefinedService()</span><span class="sxs-lookup"><span data-stu-id="63d8c-939">public boolean getUsePredefinedService()</span></span>              | <span data-ttu-id="63d8c-940">loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-940">Returns whether the loginProperty class is set to use a predefined Oracle service instead of specifying the server and database information on the loginProperty class.</span></span>                                |
| <span data-ttu-id="63d8c-941">public void setTcpIpPort(str tcpipPort)</span><span class="sxs-lookup"><span data-stu-id="63d8c-941">public void setTcpIpPort(str tcpipPort)</span></span>               | <span data-ttu-id="63d8c-942">Oracle に接続するために使用される TCP/IP ポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-942">Specifies which TCP/IP port is used to connect to Oracle.</span></span>                                                                                                                                              |
| <span data-ttu-id="63d8c-943">public void setDatabase(str database)</span><span class="sxs-lookup"><span data-stu-id="63d8c-943">public void setDatabase(str database)</span></span>                 | <span data-ttu-id="63d8c-944">ログイン先のデータベースの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-944">Sets the name of the database to log on to.</span></span>                                                                                                                                                            |
| <span data-ttu-id="63d8c-945">public void setDSN(str datasourceName)</span><span class="sxs-lookup"><span data-stu-id="63d8c-945">public void setDSN(str datasourceName)</span></span>                | <span data-ttu-id="63d8c-946">データ ソースへのアクセスに使用される DSN を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-946">Sets the DSN that is used to access the data source.</span></span>                                                                                                                                                   |
| <span data-ttu-id="63d8c-947">public void new()</span><span class="sxs-lookup"><span data-stu-id="63d8c-947">public void new()</span></span>                                     | <span data-ttu-id="63d8c-948">LoginProperty クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-948">Initializes a new instance of the LoginProperty class.</span></span>                                                                                                                                                 |
| <span data-ttu-id="63d8c-949">public void setOciServiceName(str ociServiceName)</span><span class="sxs-lookup"><span data-stu-id="63d8c-949">public void setOciServiceName(str ociServiceName)</span></span>     | <span data-ttu-id="63d8c-950">Oracle サービス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-950">Specifies an Oracle service name.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="63d8c-951">public void setOther(str otherOdbcParameters)</span><span class="sxs-lookup"><span data-stu-id="63d8c-951">public void setOther(str otherOdbcParameters)</span></span>         | <span data-ttu-id="63d8c-952">LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-952">Sets additional nonstandard logon parameters that are stored in the LoginProperty class.</span></span>                                                                                                               |
| <span data-ttu-id="63d8c-953">public void setServer(str serverName)</span><span class="sxs-lookup"><span data-stu-id="63d8c-953">public void setServer(str serverName)</span></span>                 | <span data-ttu-id="63d8c-954">データベースが置かれているサーバーの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-954">Sets the name of the server on which the database resides.</span></span>                                                                                                                                             |
| <span data-ttu-id="63d8c-955">public void setUsePredefinedService(boolean newValue)</span><span class="sxs-lookup"><span data-stu-id="63d8c-955">public void setUsePredefinedService(boolean newValue)</span></span> | <span data-ttu-id="63d8c-956">接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-956">Specifies whether to use a predefined Oracle service (created by using Oracle network configuration tools) for the connection information, or whether it will be specified in the loginProperty class.</span></span> |

### <a name="method-getdatabase"></a><span data-ttu-id="63d8c-957">メソッド getDatabase</span><span class="sxs-lookup"><span data-stu-id="63d8c-957">Method getDatabase</span></span>

<span data-ttu-id="63d8c-958">LoginProperty クラスに格納されている、データベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-958">Retrieves the name of the database, as stored in the LoginProperty class.</span></span>

    public str getDatabase()

#### <a name="return-value"></a><span data-ttu-id="63d8c-959">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-959">Return Value</span></span>

<span data-ttu-id="63d8c-960">データベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-960">The name of the database.</span></span>

### <a name="method-getdsn"></a><span data-ttu-id="63d8c-961">メソッド getDSN</span><span class="sxs-lookup"><span data-stu-id="63d8c-961">Method getDSN</span></span>

<span data-ttu-id="63d8c-962">LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-962">Retrieves the data source name (DSN) that is stored in the LoginProperty class.</span></span>

    public str getDSN()

#### <a name="return-value"></a><span data-ttu-id="63d8c-963">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-963">Return Value</span></span>

<span data-ttu-id="63d8c-964">DSN。</span><span class="sxs-lookup"><span data-stu-id="63d8c-964">The DSN.</span></span>

### <a name="method-getociservicename"></a><span data-ttu-id="63d8c-965">メソッド getOciServiceName</span><span class="sxs-lookup"><span data-stu-id="63d8c-965">Method getOciServiceName</span></span>

<span data-ttu-id="63d8c-966">LoginProperty クラスに格納されている Oracle サービス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-966">Retrieves the Oracle service name that is stored in the LoginProperty class.</span></span>

    public str getOciServiceName()

#### <a name="return-value"></a><span data-ttu-id="63d8c-967">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-967">Return Value</span></span>

<span data-ttu-id="63d8c-968">Oracle サービス名。</span><span class="sxs-lookup"><span data-stu-id="63d8c-968">The Oracle service name.</span></span>

### <a name="method-getother"></a><span data-ttu-id="63d8c-969">メソッド getOther</span><span class="sxs-lookup"><span data-stu-id="63d8c-969">Method getOther</span></span>

<span data-ttu-id="63d8c-970">LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-970">Retrieves the additional logon parameters that are stored in the LoginProperty class.</span></span>

    public str getOther()

#### <a name="return-value"></a><span data-ttu-id="63d8c-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-971">Return Value</span></span>

<span data-ttu-id="63d8c-972">文字列としての追加ログオン パラメーター。</span><span class="sxs-lookup"><span data-stu-id="63d8c-972">The additional logon parameters as a string.</span></span>

### <a name="method-getserver"></a><span data-ttu-id="63d8c-973">メソッド getServer</span><span class="sxs-lookup"><span data-stu-id="63d8c-973">Method getServer</span></span>

<span data-ttu-id="63d8c-974">LoginProperty クラスに格納されているサーバー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-974">Retrieves the server name that is stored in the LoginProperty class.</span></span>

    public str getServer()

#### <a name="return-value"></a><span data-ttu-id="63d8c-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-975">Return Value</span></span>

<span data-ttu-id="63d8c-976">サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="63d8c-976">The name of the server.</span></span>

### <a name="method-gettcpipport"></a><span data-ttu-id="63d8c-977">メソッド getTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="63d8c-977">Method getTcpIpPort</span></span>

<span data-ttu-id="63d8c-978">LoginProperty クラスに格納されている TCP/IP ポートを取得します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-978">Retrieves the TCP/IP port that is stored in the LoginProperty class.</span></span>

    public str getTcpIpPort()

#### <a name="return-value"></a><span data-ttu-id="63d8c-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-979">Return Value</span></span>

<span data-ttu-id="63d8c-980">TCP/IP ポート。</span><span class="sxs-lookup"><span data-stu-id="63d8c-980">The TCP/IP port.</span></span>

### <a name="method-getusepredefinedservice"></a><span data-ttu-id="63d8c-981">メソッド getUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="63d8c-981">Method getUsePredefinedService</span></span>

<span data-ttu-id="63d8c-982">loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-982">Returns whether the loginProperty class is set to use a predefined Oracle service instead of specifying the server and database information on the loginProperty class.</span></span>

    public boolean getUsePredefinedService()

#### <a name="return-value"></a><span data-ttu-id="63d8c-983">戻り値</span><span class="sxs-lookup"><span data-stu-id="63d8c-983">Return Value</span></span>

<span data-ttu-id="63d8c-984">定義済みの Oracle サービスが接続に使用される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="63d8c-984">true if a predefined Oracle service is used to connect; otherwise, false.</span></span>

### <a name="method-settcpipport"></a><span data-ttu-id="63d8c-985">メソッド setTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="63d8c-985">Method setTcpIpPort</span></span>

<span data-ttu-id="63d8c-986">Oracle に接続するために使用される TCP/IP ポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-986">Specifies which TCP/IP port is used to connect to Oracle.</span></span>

    public void setTcpIpPort(str tcpipPort)

#### <a name="parameters"></a><span data-ttu-id="63d8c-987">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-987">Parameters</span></span>

<span data-ttu-id="63d8c-988">tcpipPort</span><span class="sxs-lookup"><span data-stu-id="63d8c-988">tcpipPort</span></span>  
<span data-ttu-id="63d8c-989">使用する TCP/IP ポート。</span><span class="sxs-lookup"><span data-stu-id="63d8c-989">The TCP/IP port to use.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-990">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-990">Remarks</span></span>

<span data-ttu-id="63d8c-991">既定のポートは 1521 です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-991">The default port is 1521.</span></span>

### <a name="method-setdatabase"></a><span data-ttu-id="63d8c-992">メソッド setDatabase</span><span class="sxs-lookup"><span data-stu-id="63d8c-992">Method setDatabase</span></span>

<span data-ttu-id="63d8c-993">ログイン先のデータベースの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-993">Sets the name of the database to log on to.</span></span>

    public void setDatabase(str database)

#### <a name="parameters"></a><span data-ttu-id="63d8c-994">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-994">Parameters</span></span>

<span data-ttu-id="63d8c-995">データベース</span><span class="sxs-lookup"><span data-stu-id="63d8c-995">database</span></span>  
<span data-ttu-id="63d8c-996">データベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="63d8c-996">The name of the database.</span></span>

### <a name="method-setdsn"></a><span data-ttu-id="63d8c-997">メソッド setDSN</span><span class="sxs-lookup"><span data-stu-id="63d8c-997">Method setDSN</span></span>

<span data-ttu-id="63d8c-998">データ ソースへのアクセスに使用される DSN を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-998">Sets the DSN that is used to access the data source.</span></span>

    public void setDSN(str datasourceName)

#### <a name="parameters"></a><span data-ttu-id="63d8c-999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-999">Parameters</span></span>

<span data-ttu-id="63d8c-1000">datasourceName</span><span class="sxs-lookup"><span data-stu-id="63d8c-1000">datasourceName</span></span>  
<span data-ttu-id="63d8c-1001">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1001">The name of the data source.</span></span>

### <a name="method-new"></a><span data-ttu-id="63d8c-1002">メソッド new</span><span class="sxs-lookup"><span data-stu-id="63d8c-1002">Method new</span></span>

<span data-ttu-id="63d8c-1003">LoginProperty クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1003">Initializes a new instance of the LoginProperty class.</span></span>

    public void new()

### <a name="method-setociservicename"></a><span data-ttu-id="63d8c-1004">メソッド setOciServiceName</span><span class="sxs-lookup"><span data-stu-id="63d8c-1004">Method setOciServiceName</span></span>

<span data-ttu-id="63d8c-1005">Oracle サービス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1005">Specifies an Oracle service name.</span></span>

    public void setOciServiceName(str ociServiceName)

#### <a name="parameters"></a><span data-ttu-id="63d8c-1006">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-1006">Parameters</span></span>

<span data-ttu-id="63d8c-1007">ociServiceName</span><span class="sxs-lookup"><span data-stu-id="63d8c-1007">ociServiceName</span></span>  
<span data-ttu-id="63d8c-1008">サービスの名前。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1008">The name of the service.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-1009">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-1009">Remarks</span></span>

<span data-ttu-id="63d8c-1010">このメソッドは、loginProperty クラスが事前定義済みの Oracle サービスを使用するように設定されていない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1010">This method is used when the loginProperty class is not set to use a predefined Oracle service.</span></span>

### <a name="method-setother"></a><span data-ttu-id="63d8c-1011">メソッド setOther</span><span class="sxs-lookup"><span data-stu-id="63d8c-1011">Method setOther</span></span>

<span data-ttu-id="63d8c-1012">LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1012">Sets additional nonstandard logon parameters that are stored in the LoginProperty class.</span></span>

    public void setOther(str otherOdbcParameters)

#### <a name="parameters"></a><span data-ttu-id="63d8c-1013">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-1013">Parameters</span></span>

<span data-ttu-id="63d8c-1014">otherOdbcParameters</span><span class="sxs-lookup"><span data-stu-id="63d8c-1014">otherOdbcParameters</span></span>  
<span data-ttu-id="63d8c-1015">ODBC 書式に設定された追加のパラメータ。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1015">The additional ODBC-formatted parameters.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-1016">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-1016">Remarks</span></span>

<span data-ttu-id="63d8c-1017">このメソッドは、使用するデータソースに追加の非標準のパラメーターが必要な場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1017">This method should be used only if the data source that you want to use requires some additional, nonstandard parameters.</span></span> <span data-ttu-id="63d8c-1018">パラメーターは、標準の ODBC 形式の &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt; で、たとえば、MODE=1;PATCH=32 で適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1018">The parameters must be applied in the standard ODBC format: &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt;,... For example: MODE=1;PATCH=32</span></span>

### <a name="method-setserver"></a><span data-ttu-id="63d8c-1019">メソッド setServer</span><span class="sxs-lookup"><span data-stu-id="63d8c-1019">Method setServer</span></span>

<span data-ttu-id="63d8c-1020">データベースが置かれているサーバーの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1020">Sets the name of the server on which the database resides.</span></span>

    public void setServer(str serverName)

#### <a name="parameters"></a><span data-ttu-id="63d8c-1021">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-1021">Parameters</span></span>

<span data-ttu-id="63d8c-1022">serverName</span><span class="sxs-lookup"><span data-stu-id="63d8c-1022">serverName</span></span>  
<span data-ttu-id="63d8c-1023">データベースがあるサーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1023">The name of the server where the database is located.</span></span>

### <a name="method-setusepredefinedservice"></a><span data-ttu-id="63d8c-1024">メソッド setUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="63d8c-1024">Method setUsePredefinedService</span></span>

<span data-ttu-id="63d8c-1025">接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1025">Specifies whether to use a predefined Oracle service (created by using Oracle network configuration tools) for the connection information, or whether it will be specified in the loginProperty class.</span></span>

    public void setUsePredefinedService(boolean newValue)

#### <a name="parameters"></a><span data-ttu-id="63d8c-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63d8c-1026">Parameters</span></span>

<span data-ttu-id="63d8c-1027">newValue</span><span class="sxs-lookup"><span data-stu-id="63d8c-1027">newValue</span></span>  
<span data-ttu-id="63d8c-1028">事前定義された Oracle サービスを使用するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1028">A Boolean value that indicates whether to use a predefined Oracle service.</span></span>

#### <a name="remarks"></a><span data-ttu-id="63d8c-1029">備考</span><span class="sxs-lookup"><span data-stu-id="63d8c-1029">Remarks</span></span>

<span data-ttu-id="63d8c-1030">既定では、事前に定義されたサービスは使用されません。</span><span class="sxs-lookup"><span data-stu-id="63d8c-1030">By default, a predefined service is not used.</span></span>


