---
title: 'Label クラス '
description: このトピックでは、Label クラスについて説明します。
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
ms.openlocfilehash: bd2d63127d839ec1cde16650d0b50707f9e10319
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502592"
---
# <a name="class-label"></a><span data-ttu-id="93bfa-103">クラス ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-103">Class Label</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Label extends Object
```

<span data-ttu-id="93bfa-104">Label クラスは、ラベル ID およびラベル ファイルを管理します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-104">The Label class manages label IDs and label files.</span></span>

## <a name="remarks"></a><span data-ttu-id="93bfa-105">備考</span><span class="sxs-lookup"><span data-stu-id="93bfa-105">Remarks</span></span>

<span data-ttu-id="93bfa-106">SysLabel クラスは、Label クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-106">The SysLabel class extends the Label class.</span></span>

## <a name="examples"></a><span data-ttu-id="93bfa-107">例</span><span class="sxs-lookup"><span data-stu-id="93bfa-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="93bfa-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="93bfa-108">Methods</span></span>

| <span data-ttu-id="93bfa-109">方法</span><span class="sxs-lookup"><span data-stu-id="93bfa-109">Method</span></span>                                                                | <span data-ttu-id="93bfa-110">説明</span><span class="sxs-lookup"><span data-stu-id="93bfa-110">Description</span></span>                                                                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bfa-111">public LabelBulkEditor bulkEditor(str module)</span><span class="sxs-lookup"><span data-stu-id="93bfa-111">public LabelBulkEditor bulkEditor(str module)</span></span>                         | <span data-ttu-id="93bfa-112">LabelBulkEditor クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-112">Creates an instance of the LabelBulkEditor class.</span></span>                                                   |
| <span data-ttu-id="93bfa-113">public boolean createLabelFile(str module, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-113">public boolean createLabelFile(str module, str language)</span></span>              | <span data-ttu-id="93bfa-114">指定されたラベル ID のラベル ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-114">Creates a label file for a specified label ID.</span></span>                                                      |
| <span data-ttu-id="93bfa-115">public boolean delete(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-115">public boolean delete(str label)</span></span>                                      | <span data-ttu-id="93bfa-116">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-116">Deletes a specified label.</span></span>                                                                          |
| <span data-ttu-id="93bfa-117">public boolean exists(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-117">public boolean exists(str label)</span></span>                                      | <span data-ttu-id="93bfa-118">指定したラベル ID が存在するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-118">Indicates whether a specified label ID exists.</span></span>                                                      |
| <span data-ttu-id="93bfa-119">public str extractComment(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-119">public str extractComment(str label)</span></span>                                  | <span data-ttu-id="93bfa-120">指定されたラベル ID に関連付けられているコメントを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-120">Returns a comment that is associated with a specified label ID.</span></span>                                     |
| <span data-ttu-id="93bfa-121">public str extractString(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-121">public str extractString(str label)</span></span>                                   | <span data-ttu-id="93bfa-122">指定されたラベル ID に関連付けられているテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-122">Returns the text that is associated with a specified label ID.</span></span>                                      |
| <span data-ttu-id="93bfa-123">public str getFirstLabelFile()</span><span class="sxs-lookup"><span data-stu-id="93bfa-123">public str getFirstLabelFile()</span></span>                                        | <span data-ttu-id="93bfa-124">最初のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-124">Returns the first label file ID record.</span></span>                                                             |
| <span data-ttu-id="93bfa-125">public Date getLabelFileCreatedDate(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-125">public Date getLabelFileCreatedDate(str labelFile, str language)</span></span>      | <span data-ttu-id="93bfa-126">指定したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-126">Returns the date that a specified label file was created.</span></span>                                           |
| <span data-ttu-id="93bfa-127">public int getLabelFileCreatedTime(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-127">public int getLabelFileCreatedTime(str labelFile, str language)</span></span>       | <span data-ttu-id="93bfa-128">指定したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-128">Returns the time that a specified label file was created.</span></span>                                           |
| <span data-ttu-id="93bfa-129">public Date getLabelFileModificationDate(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-129">public Date getLabelFileModificationDate(str labelFile, str language)</span></span> | <span data-ttu-id="93bfa-130">変更したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-130">Returns the date that a specified label file was modified.</span></span>                                          |
| <span data-ttu-id="93bfa-131">public int getLabelFileModificationTime(str labelFile, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-131">public int getLabelFileModificationTime(str labelFile, str language)</span></span>  | <span data-ttu-id="93bfa-132">変更したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-132">Returns the time that a specified label file was modified.</span></span>                                          |
| <span data-ttu-id="93bfa-133">public str getNextLabelFile()</span><span class="sxs-lookup"><span data-stu-id="93bfa-133">public str getNextLabelFile()</span></span>                                         | <span data-ttu-id="93bfa-134">次のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-134">Returns the next label file ID record.</span></span>                                                              |
| <span data-ttu-id="93bfa-135">public str insert(str text, str comment, str module)</span><span class="sxs-lookup"><span data-stu-id="93bfa-135">public str insert(str text, str comment, str module)</span></span>                  | <span data-ttu-id="93bfa-136">指定されたテキスト文字列のラベル ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-136">Creates a label ID for a specified text string.</span></span>                                                     |
| <span data-ttu-id="93bfa-137">public int labelId(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-137">public int labelId(str label)</span></span>                                         | <span data-ttu-id="93bfa-138">指定したラベル ID に含まれる番号を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-138">Returns the number that is included in a specified label ID.</span></span>                                        |
| <span data-ttu-id="93bfa-139">public int maxLabelId(str module)</span><span class="sxs-lookup"><span data-stu-id="93bfa-139">public int maxLabelId(str module)</span></span>                                     | <span data-ttu-id="93bfa-140">指定したラベル ファイル内の最後のラベルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-140">Returns the ID for the last label in the specified label file.</span></span>                                      |
| <span data-ttu-id="93bfa-141">public boolean modify(str label, str text, \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="93bfa-141">public boolean modify(str label, str text, \[str comment\])</span></span>           | <span data-ttu-id="93bfa-142">指定されたラベルに関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-142">Modifies the text and comment that are associated with a specified label.</span></span>                           |
| <span data-ttu-id="93bfa-143">public str moduleId(str label)</span><span class="sxs-lookup"><span data-stu-id="93bfa-143">public str moduleId(str label)</span></span>                                        | <span data-ttu-id="93bfa-144">指定したラベル ID のラベル ファイルを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-144">Returns the label file ID for a specified label ID.</span></span>                                                 |
| <span data-ttu-id="93bfa-145">public boolean moreLabelFiles()</span><span class="sxs-lookup"><span data-stu-id="93bfa-145">public boolean moreLabelFiles()</span></span>                                       | <span data-ttu-id="93bfa-146">追加のラベル ファイルがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-146">Indicates whether there are additional label files.</span></span>                                                 |
| <span data-ttu-id="93bfa-147">public str name(str module, int labelId)</span><span class="sxs-lookup"><span data-stu-id="93bfa-147">public str name(str module, int labelId)</span></span>                              | <span data-ttu-id="93bfa-148">指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-148">Returns a label ID, based on a specified label file ID and label ID number.</span></span>                         |
| <span data-ttu-id="93bfa-149">public str searchFirst(str searchString)</span><span class="sxs-lookup"><span data-stu-id="93bfa-149">public str searchFirst(str searchString)</span></span>                              | <span data-ttu-id="93bfa-150">指定した検索用語で検出された最初のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-150">Returns the first label ID that is found for a specified search term.</span></span>                               |
| <span data-ttu-id="93bfa-151">public str searchNext()</span><span class="sxs-lookup"><span data-stu-id="93bfa-151">public str searchNext()</span></span>                                               | <span data-ttu-id="93bfa-152">searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-152">Returns the next label ID that is found for a search term that is passed to the searchFirst method.</span></span> |
| <span data-ttu-id="93bfa-153">::public static boolean flush(str labelFileId, str language)</span><span class="sxs-lookup"><span data-stu-id="93bfa-153">::public static boolean flush(str labelFileId, str language)</span></span>          | <span data-ttu-id="93bfa-154">ディスクにラベル ファイル バッファーをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="93bfa-154">Flushes the label file buffers to disk.</span></span>                                                             |
| <span data-ttu-id="93bfa-155">public void new(\[str language\])</span><span class="sxs-lookup"><span data-stu-id="93bfa-155">public void new(\[str language\])</span></span>                                     | <span data-ttu-id="93bfa-156">ラベル クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-156">Creates a new instance of the Label class.</span></span>                                                          |
| <span data-ttu-id="93bfa-157">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="93bfa-157">public void finalize()</span></span>                                                | <span data-ttu-id="93bfa-158">現在のラベル ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-158">Closes the current label file.</span></span>                                                                      |

## <a name="method-bulkeditor"></a><span data-ttu-id="93bfa-159">メソッド bulkEditor</span><span class="sxs-lookup"><span data-stu-id="93bfa-159">Method bulkEditor</span></span>

<span data-ttu-id="93bfa-160">LabelBulkEditor クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-160">Creates an instance of the LabelBulkEditor class.</span></span>

```xpp
public LabelBulkEditor bulkEditor(str module)
```

### <a name="parameters---bulkeditor"></a><span data-ttu-id="93bfa-161">パラメータ - bulkEditor</span><span class="sxs-lookup"><span data-stu-id="93bfa-161">Parameters - bulkEditor</span></span>

<span data-ttu-id="93bfa-162">モジュール</span><span class="sxs-lookup"><span data-stu-id="93bfa-162">module</span></span>  
<span data-ttu-id="93bfa-163">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-163">A string data type that specifies a three-letter label file ID.</span></span>

### <a name="return-value---bulkeditor"></a><span data-ttu-id="93bfa-164">戻り値 - bulkEditor</span><span class="sxs-lookup"><span data-stu-id="93bfa-164">Return Value - bulkEditor</span></span>

<span data-ttu-id="93bfa-165">LabelBulkEditor クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="93bfa-165">An instance of the LabelBulkEditor class.</span></span>

### <a name="remarks---bulkeditor"></a><span data-ttu-id="93bfa-166">備考 - bulkEditor</span><span class="sxs-lookup"><span data-stu-id="93bfa-166">Remarks - bulkEditor</span></span>

<span data-ttu-id="93bfa-167">LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-167">The LabelBulkEditor class is used to quickly modify a label file.</span></span> <span data-ttu-id="93bfa-168">このメソッドは、クライアント層から呼び出されたときに nullNothingnullptrunita null 参照 (Visual Basic ではNothing) を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-168">This method returns nullNothingnullptrunita null reference (Nothing in Visual Basic) when it is invoked from the client tier.</span></span>

## <a name="method-createlabelfile"></a><span data-ttu-id="93bfa-169">メソッド createLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-169">Method createLabelFile</span></span>

<span data-ttu-id="93bfa-170">指定されたラベル ID のラベル ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-170">Creates a label file for a specified label ID.</span></span>

```xpp
public boolean createLabelFile(str module, str language)
```

### <a name="parameters---createlabelfile"></a><span data-ttu-id="93bfa-171">パラメーター - createLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-171">Parameters - createLabelFile</span></span>

<span data-ttu-id="93bfa-172">モジュール</span><span class="sxs-lookup"><span data-stu-id="93bfa-172">module</span></span>  
<span data-ttu-id="93bfa-173">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-173">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-174">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-174">language</span></span>  
<span data-ttu-id="93bfa-175">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-175">A string data type that specifies a language by using a language prefix.</span></span>

### <a name="return-value---createlabelfile"></a><span data-ttu-id="93bfa-176">戻り値 - createLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-176">Return Value - createLabelFile</span></span>

<span data-ttu-id="93bfa-177">ファイルが作成された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="93bfa-177">true if a file is created; otherwise, false.</span></span>

### <a name="remarks---createlabelfile"></a><span data-ttu-id="93bfa-178">備考 - createLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-178">Remarks - createLabelFile</span></span>

<span data-ttu-id="93bfa-179">ラベル ファイルは、ファイル バッファがディスクにフラッシュされた後に作成されます。これは、サーバーが閉じるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-179">The label file is created after the file buffers are flushed to disk, which occurs when the server closes.</span></span>

## <a name="method-delete"></a><span data-ttu-id="93bfa-180">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="93bfa-180">Method delete</span></span>

<span data-ttu-id="93bfa-181">指定したラベルを削除します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-181">Deletes a specified label.</span></span>

```xpp
public boolean delete(str label)
```

### <a name="parameters---delete"></a><span data-ttu-id="93bfa-182">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="93bfa-182">Parameters - delete</span></span>

<span data-ttu-id="93bfa-183">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-183">label</span></span>  
<span data-ttu-id="93bfa-184">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-184">A string that specifies the label ID.</span></span> <span data-ttu-id="93bfa-185">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-185">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---delete"></a><span data-ttu-id="93bfa-186">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="93bfa-186">Return Value - delete</span></span>

<span data-ttu-id="93bfa-187">ラベル ID が削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="93bfa-187">true if the label ID is deleted; otherwise, false.</span></span>

## <a name="method-exists"></a><span data-ttu-id="93bfa-188">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="93bfa-188">Method exists</span></span>

<span data-ttu-id="93bfa-189">指定したラベル ID が存在するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-189">Indicates whether a specified label ID exists.</span></span>

```xpp
public boolean exists(str label)
```

### <a name="parameters---exists"></a><span data-ttu-id="93bfa-190">パラメーター - exists</span><span class="sxs-lookup"><span data-stu-id="93bfa-190">Parameters - exists</span></span>

<span data-ttu-id="93bfa-191">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-191">label</span></span>  
<span data-ttu-id="93bfa-192">アット マーク (@) を含むラベル ID 文字列からの literalStr 関数の出力。</span><span class="sxs-lookup"><span data-stu-id="93bfa-192">The output of the literalStr function from a label ID string that includes the at sign (@).</span></span>

### <a name="return-value---exists"></a><span data-ttu-id="93bfa-193">戻り値 - exists</span><span class="sxs-lookup"><span data-stu-id="93bfa-193">Return Value - exists</span></span>

<span data-ttu-id="93bfa-194">ラベル ID が存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="93bfa-194">true if the label ID exists; otherwise, false.</span></span>

### <a name="remarks---exists"></a><span data-ttu-id="93bfa-195">備考 - exists</span><span class="sxs-lookup"><span data-stu-id="93bfa-195">Remarks - exists</span></span>

<span data-ttu-id="93bfa-196">ラベル パラメーターの値の形式は、literalStr と同様でなければいけません ("@SYS24359")。</span><span class="sxs-lookup"><span data-stu-id="93bfa-196">The format of the label parameter value must resemble literalStr("@SYS24359").</span></span>

## <a name="method-extractcomment"></a><span data-ttu-id="93bfa-197">メソッド extractComment</span><span class="sxs-lookup"><span data-stu-id="93bfa-197">Method extractComment</span></span>

<span data-ttu-id="93bfa-198">指定されたラベル ID に関連付けられているコメントを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-198">Returns a comment that is associated with a specified label ID.</span></span>

```xpp
public str extractComment(str label)
```

### <a name="parameters---extractcomment"></a><span data-ttu-id="93bfa-199">パラメーター - extractComment</span><span class="sxs-lookup"><span data-stu-id="93bfa-199">Parameters - extractComment</span></span>

<span data-ttu-id="93bfa-200">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-200">label</span></span>  
<span data-ttu-id="93bfa-201">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-201">A string that specifies the label ID.</span></span> <span data-ttu-id="93bfa-202">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-202">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---extractcomment"></a><span data-ttu-id="93bfa-203">戻り値 - extractComment</span><span class="sxs-lookup"><span data-stu-id="93bfa-203">Return Value - extractComment</span></span>

<span data-ttu-id="93bfa-204">指定されたラベル ID に関連付けられているコメントを示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-204">A string value that indicates the comment that is associated with the specified label ID.</span></span>

### <a name="remarks---extractcomment"></a><span data-ttu-id="93bfa-205">備考 - extractComment</span><span class="sxs-lookup"><span data-stu-id="93bfa-205">Remarks - extractComment</span></span>

<span data-ttu-id="93bfa-206">存在しないラベル ID を指定する場合、このメソッドは文字列として指定した ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-206">If you specify a label ID that does not exist, this method returns the specified ID as a string.</span></span> <span data-ttu-id="93bfa-207">ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-207">If you do not include the @ in the label parameter value, the method returns the label ID.</span></span>

## <a name="method-extractstring"></a><span data-ttu-id="93bfa-208">メソッド extractString</span><span class="sxs-lookup"><span data-stu-id="93bfa-208">Method extractString</span></span>

<span data-ttu-id="93bfa-209">指定されたラベル ID に関連付けられているテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-209">Returns the text that is associated with a specified label ID.</span></span>

```xpp
public str extractString(str label)
```

### <a name="parameters---extractstring"></a><span data-ttu-id="93bfa-210">パラメーター - extractString</span><span class="sxs-lookup"><span data-stu-id="93bfa-210">Parameters - extractString</span></span>

<span data-ttu-id="93bfa-211">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-211">label</span></span>  
<span data-ttu-id="93bfa-212">ラベル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-212">A string data type that specifies a label ID.</span></span> <span data-ttu-id="93bfa-213">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-213">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---extractstring"></a><span data-ttu-id="93bfa-214">戻り値 - extractString</span><span class="sxs-lookup"><span data-stu-id="93bfa-214">Return Value - extractString</span></span>

<span data-ttu-id="93bfa-215">指定されたラベル ID に関連付けられているテキストを示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-215">A string data type value that indicates the text that is associated with the specified label ID.</span></span>

### <a name="remarks---extractstring"></a><span data-ttu-id="93bfa-216">備考 - extractString</span><span class="sxs-lookup"><span data-stu-id="93bfa-216">Remarks - extractString</span></span>

<span data-ttu-id="93bfa-217">存在しないラベル ID を指定する場合、メソッドは文字列として指定した ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-217">If you specify a label ID that does not exist, the method returns the specified ID as a string.</span></span> <span data-ttu-id="93bfa-218">ラベル パラメーターの値に @ を含めない場合は、メソッドはラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-218">If you do not include the @ in the label parameter value, the method returns the label ID.</span></span>

## <a name="method-getfirstlabelfile"></a><span data-ttu-id="93bfa-219">メソッド getFirstLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-219">Method getFirstLabelFile</span></span>

<span data-ttu-id="93bfa-220">最初のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-220">Returns the first label file ID record.</span></span>

```xpp
public str getFirstLabelFile()
```

### <a name="return-value---getfirstlabelfile"></a><span data-ttu-id="93bfa-221">戻り値 - getFirstLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-221">Return Value - getFirstLabelFile</span></span>

<span data-ttu-id="93bfa-222">ラベル ファイル ID を示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-222">A string data type value that indicates the label file ID.</span></span>

### <a name="remarks---getfirstlabelfile"></a><span data-ttu-id="93bfa-223">備考 - getFirstLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-223">Remarks - getFirstLabelFile</span></span>

<span data-ttu-id="93bfa-224">ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。</span><span class="sxs-lookup"><span data-stu-id="93bfa-224">A label file ID is a three-letter identifier for a label file.</span></span>

## <a name="method-getlabelfilecreateddate"></a><span data-ttu-id="93bfa-225">メソッド getLabelFileCreatedDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-225">Method getLabelFileCreatedDate</span></span>

<span data-ttu-id="93bfa-226">指定したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-226">Returns the date that a specified label file was created.</span></span>

```xpp
public Date getLabelFileCreatedDate(str labelFile, str language)
```

### <a name="parameters---getlabelfilecreateddate"></a><span data-ttu-id="93bfa-227">パラメーター - getLabelFileCreatedDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-227">Parameters - getLabelFileCreatedDate</span></span>

<span data-ttu-id="93bfa-228">labelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-228">labelFile</span></span>  
<span data-ttu-id="93bfa-229">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-229">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-230">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-230">language</span></span>  
<span data-ttu-id="93bfa-231">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-231">A string data type that specifies a language by using a language prefix.</span></span>

### <a name="return-value---getlabelfilecreateddate"></a><span data-ttu-id="93bfa-232">戻り値 - getLabelFileCreatedDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-232">Return Value - getLabelFileCreatedDate</span></span>

<span data-ttu-id="93bfa-233">ラベル ファイルの作成日時を示す Date データ タイプ値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-233">A Date data type value that indicates when a label file is created.</span></span>

### <a name="remarks---getlabelfilecreateddate"></a><span data-ttu-id="93bfa-234">備考 - getLabelFileCreatedDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-234">Remarks - getLabelFileCreatedDate</span></span>

<span data-ttu-id="93bfa-235">date2str 関数を使用すると日付をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-235">You can use the date2str function to convert the date to a text string.</span></span>

## <a name="method-getlabelfilecreatedtime"></a><span data-ttu-id="93bfa-236">メソッド getLabelFileCreatedTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-236">Method getLabelFileCreatedTime</span></span>

<span data-ttu-id="93bfa-237">指定したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-237">Returns the time that a specified label file was created.</span></span>

```xpp
public int getLabelFileCreatedTime(str labelFile, str language)
```

### <a name="parameters---getlabelfilecreatedtime"></a><span data-ttu-id="93bfa-238">パラメーター - getLabelFileCreatedTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-238">Parameters - getLabelFileCreatedTime</span></span>

<span data-ttu-id="93bfa-239">labelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-239">labelFile</span></span>  
<span data-ttu-id="93bfa-240">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-240">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-241">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-241">language</span></span>  
<span data-ttu-id="93bfa-242">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-242">A string data type that specifies a language by using a language prefix.</span></span>

### <a name="return-value---getlabelfilecreatedtime"></a><span data-ttu-id="93bfa-243">戻り値 - getLabelFileCreatedTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-243">Return Value - getLabelFileCreatedTime</span></span>

<span data-ttu-id="93bfa-244">ラベル ファイルが作成された時間を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-244">An integer data type value that indicates the time that a label file is created.</span></span>

### <a name="remarks---getlabelfilecreatedtime"></a><span data-ttu-id="93bfa-245">備考 - getLabelFileCreatedTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-245">Remarks - getLabelFileCreatedTime</span></span>

<span data-ttu-id="93bfa-246">詳細については、「方法: ラベル ファイルの作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93bfa-246">For more information, see How to: Create a Label File.</span></span> <span data-ttu-id="93bfa-247">time2str 関数を使用すると整数をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-247">You can use the time2str function to convert the integer to a text string.</span></span>

## <a name="method-getlabelfilemodificationdate"></a><span data-ttu-id="93bfa-248">メソッド getLabelFileModificationDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-248">Method getLabelFileModificationDate</span></span>

<span data-ttu-id="93bfa-249">変更したラベル ファイルが作成された日付を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-249">Returns the date that a specified label file was modified.</span></span>

```xpp
public Date getLabelFileModificationDate(str labelFile, str language)
```

### <a name="parameters---getlabelfilemodificationdate"></a><span data-ttu-id="93bfa-250">パラメーター - getLabelFileModificationDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-250">Parameters - getLabelFileModificationDate</span></span>

<span data-ttu-id="93bfa-251">labelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-251">labelFile</span></span>  
<span data-ttu-id="93bfa-252">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-252">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-253">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-253">language</span></span>  
<span data-ttu-id="93bfa-254">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-254">A string data type that specifies a language by using a language prefix.</span></span>

### <a name="return-value---getlabelfilemodificationdate"></a><span data-ttu-id="93bfa-255">戻り値 - getLabelFileModificationDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-255">Return Value - getLabelFileModificationDate</span></span>

<span data-ttu-id="93bfa-256">ラベル ファイルの変更日時を示す Date データ タイプ値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-256">A Date data type value that indicates when a label file was modified.</span></span>

### <a name="remarks---getlabelfilemodificationdate"></a><span data-ttu-id="93bfa-257">戻り値 - getLabelFileModificationDate</span><span class="sxs-lookup"><span data-stu-id="93bfa-257">Remarks - getLabelFileModificationDate</span></span>

<span data-ttu-id="93bfa-258">date2str 関数を使用すると日付をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-258">You can use the date2str function to convert the date to a text string.</span></span>

## <a name="method-getlabelfilemodificationtime"></a><span data-ttu-id="93bfa-259">メソッド getLabelFileModificationTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-259">Method getLabelFileModificationTime</span></span>

<span data-ttu-id="93bfa-260">変更したラベル ファイルが作成された時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-260">Returns the time that a specified label file was modified.</span></span>

```xpp
public int getLabelFileModificationTime(str labelFile, str language)
```

### <a name="parameters---getlabelfilemodificationtime"></a><span data-ttu-id="93bfa-261">パラメーター - getLabelFileModificationTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-261">Parameters - getLabelFileModificationTime</span></span>

<span data-ttu-id="93bfa-262">labelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-262">labelFile</span></span>  
<span data-ttu-id="93bfa-263">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-263">A string data type that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-264">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-264">language</span></span>  
<span data-ttu-id="93bfa-265">言語の接頭語を使用して、言語を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-265">A string data type that specifies a language by using a language prefix.</span></span>

### <a name="return-value---getlabelfilemodificationtime"></a><span data-ttu-id="93bfa-266">戻り値 - getLabelFileModificationTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-266">Return Value - getLabelFileModificationTime</span></span>

<span data-ttu-id="93bfa-267">ラベル ファイルが変更された時間を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-267">An integer value that indicates the time that a label file was modified.</span></span>

### <a name="remarks---getlabelfilemodificationtime"></a><span data-ttu-id="93bfa-268">備考 - getLabelFileModificationTime</span><span class="sxs-lookup"><span data-stu-id="93bfa-268">Remarks - getLabelFileModificationTime</span></span>

<span data-ttu-id="93bfa-269">time2str 関数を使用すると整数をテキスト文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-269">You can use the time2str function to convert the integer to a text string.</span></span>

## <a name="method-getnextlabelfile"></a><span data-ttu-id="93bfa-270">メソッド getNextLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-270">Method getNextLabelFile</span></span>

<span data-ttu-id="93bfa-271">次のラベル ファイル ID レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-271">Returns the next label file ID record.</span></span>

```xpp
public str getNextLabelFile()
```

### <a name="return-value---getnextlabelfile"></a><span data-ttu-id="93bfa-272">戻り値 - getNextLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-272">Return Value - getNextLabelFile</span></span>

<span data-ttu-id="93bfa-273">ラベル ファイル ID を示す文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-273">A string data type value that indicates the label file ID.</span></span>

### <a name="remarks---getnextlabelfile"></a><span data-ttu-id="93bfa-274">備考 - getNextLabelFile</span><span class="sxs-lookup"><span data-stu-id="93bfa-274">Remarks - getNextLabelFile</span></span>

<span data-ttu-id="93bfa-275">ラベル ファイル ID は、ラベル ファイルの 3 文字の識別子です。</span><span class="sxs-lookup"><span data-stu-id="93bfa-275">A label file ID is a three-letter identifier for a label file.</span></span>

## <a name="method-insert"></a><span data-ttu-id="93bfa-276">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="93bfa-276">Method insert</span></span>

<span data-ttu-id="93bfa-277">指定されたテキスト文字列のラベル ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-277">Creates a label ID for a specified text string.</span></span>

```xpp
public str insert(str text, str comment, str module)
```

### <a name="parameters---insert"></a><span data-ttu-id="93bfa-278">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="93bfa-278">Parameters - insert</span></span>

<span data-ttu-id="93bfa-279">テキスト</span><span class="sxs-lookup"><span data-stu-id="93bfa-279">text</span></span>  
<span data-ttu-id="93bfa-280">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-280">A string data type that specifies a three-letter label file ID.</span></span>

<!-- -->

<span data-ttu-id="93bfa-281">comment</span><span class="sxs-lookup"><span data-stu-id="93bfa-281">comment</span></span>  
<span data-ttu-id="93bfa-282">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-282">A string data type that specifies a three-letter label file ID.</span></span>

<!-- -->

<span data-ttu-id="93bfa-283">モジュール</span><span class="sxs-lookup"><span data-stu-id="93bfa-283">module</span></span>  
<span data-ttu-id="93bfa-284">3 文字のラベル ファイル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-284">A string data type that specifies a three-letter label file ID.</span></span>

### <a name="return-value---insert"></a><span data-ttu-id="93bfa-285">戻り値 - insert</span><span class="sxs-lookup"><span data-stu-id="93bfa-285">Return Value - insert</span></span>

<span data-ttu-id="93bfa-286">作成されるラベル ID の文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-286">A string data type value for the label ID that is created.</span></span>

### <a name="remarks---insert"></a><span data-ttu-id="93bfa-287">備考 - insert</span><span class="sxs-lookup"><span data-stu-id="93bfa-287">Remarks - insert</span></span>

<span data-ttu-id="93bfa-288">この操作では、すべての言語に新しいラベル ID が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-288">This operation allocates a new label ID across all languages.</span></span>

## <a name="method-labelid"></a><span data-ttu-id="93bfa-289">メソッド labelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-289">Method labelId</span></span>

<span data-ttu-id="93bfa-290">指定したラベル ID に含まれる番号を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-290">Returns the number that is included in a specified label ID.</span></span>

```xpp
public int labelId(str label)
```

### <a name="parameters---labelid"></a><span data-ttu-id="93bfa-291">パラメーター - labelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-291">Parameters - labelId</span></span>

<span data-ttu-id="93bfa-292">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-292">label</span></span>  
<span data-ttu-id="93bfa-293">ラベル ID を指定する文字列データ型。</span><span class="sxs-lookup"><span data-stu-id="93bfa-293">A string data type that specifies the label ID.</span></span> <span data-ttu-id="93bfa-294">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-294">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---labelid"></a><span data-ttu-id="93bfa-295">戻り値 - LabelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-295">Return Value - labelId</span></span>

<span data-ttu-id="93bfa-296">ラベル ID に含まれる番号を示す整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-296">An integer data type value that indicates the number that is included in a label ID.</span></span>

### <a name="remarks---labelid"></a><span data-ttu-id="93bfa-297">戻り値 - labelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-297">Remarks - labelId</span></span>

<span data-ttu-id="93bfa-298">searchFirst または searchNext メソッドを呼び出してから、パラメーターとして戻り値をこのメソッドに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-298">You must call the searchFirst or searchNext method, and then pass the return value as a parameter to this method.</span></span>

## <a name="method-maxlabelid"></a><span data-ttu-id="93bfa-299">メソッド maxLabelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-299">Method maxLabelId</span></span>

<span data-ttu-id="93bfa-300">指定したラベル ファイル内の最後のラベルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-300">Returns the ID for the last label in the specified label file.</span></span>

```xpp
public int maxLabelId(str module)
```

### <a name="parameters---maxlabelid"></a><span data-ttu-id="93bfa-301">パラメーター - maxLabelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-301">Parameters - maxLabelId</span></span>

<span data-ttu-id="93bfa-302">モジュール</span><span class="sxs-lookup"><span data-stu-id="93bfa-302">module</span></span>  
<span data-ttu-id="93bfa-303">3 文字のラベル ファイル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-303">A string that specifies a three-letter label file ID.</span></span>

### <a name="return-value---maxlabelid"></a><span data-ttu-id="93bfa-304">戻り値 - maxLabelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-304">Return Value - maxLabelId</span></span>

<span data-ttu-id="93bfa-305">指定したラベル ファイルの最大ラベル ID を示す整数。</span><span class="sxs-lookup"><span data-stu-id="93bfa-305">An integer that indicates the maximum label ID for the specified label file.</span></span>

## <a name="method-modify"></a><span data-ttu-id="93bfa-306">メソッド modify</span><span class="sxs-lookup"><span data-stu-id="93bfa-306">Method modify</span></span>

<span data-ttu-id="93bfa-307">指定されたラベルに関連付けられているテキストおよびコメントを変更します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-307">Modifies the text and comment that are associated with a specified label.</span></span>

```xpp
public boolean modify(str label, str text, [str comment])
```

### <a name="parameters---modify"></a><span data-ttu-id="93bfa-308">パラメーター - modify</span><span class="sxs-lookup"><span data-stu-id="93bfa-308">Parameters - modify</span></span>

<span data-ttu-id="93bfa-309">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-309">label</span></span>  
<span data-ttu-id="93bfa-310">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-310">A string that specifies the comment that is associated with a label ID.</span></span>

<!-- -->

<span data-ttu-id="93bfa-311">テキスト</span><span class="sxs-lookup"><span data-stu-id="93bfa-311">text</span></span>  
<span data-ttu-id="93bfa-312">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-312">A string that specifies the comment that is associated with a label ID.</span></span>

<!-- -->

<span data-ttu-id="93bfa-313">comment</span><span class="sxs-lookup"><span data-stu-id="93bfa-313">comment</span></span>  
<span data-ttu-id="93bfa-314">ラベル ID に関連付けられているコメントを指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-314">A string that specifies the comment that is associated with a label ID.</span></span>

### <a name="return-value---modify"></a><span data-ttu-id="93bfa-315">戻り値 - modify</span><span class="sxs-lookup"><span data-stu-id="93bfa-315">Return Value - modify</span></span>

<span data-ttu-id="93bfa-316">ラベル ID が修正された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="93bfa-316">true if the label ID is modified; otherwise, false.</span></span>

## <a name="method-moduleid"></a><span data-ttu-id="93bfa-317">メソッド moduleId</span><span class="sxs-lookup"><span data-stu-id="93bfa-317">Method moduleId</span></span>

<span data-ttu-id="93bfa-318">指定したラベル ID のラベル ファイルを返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-318">Returns the label file ID for a specified label ID.</span></span>

```xpp
public str moduleId(str label)
```

### <a name="parameters---moduleid"></a><span data-ttu-id="93bfa-319">パラメーター - moduleId</span><span class="sxs-lookup"><span data-stu-id="93bfa-319">Parameters - moduleId</span></span>

<span data-ttu-id="93bfa-320">ラベル</span><span class="sxs-lookup"><span data-stu-id="93bfa-320">label</span></span>  
<span data-ttu-id="93bfa-321">ラベル ID を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-321">A string that specifies the label ID.</span></span> <span data-ttu-id="93bfa-322">文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-322">The string must include the at sign (@) followed by a label file ID and a number.</span></span>

### <a name="return-value---moduleid"></a><span data-ttu-id="93bfa-323">戻り値 - moduleId</span><span class="sxs-lookup"><span data-stu-id="93bfa-323">Return Value - moduleId</span></span>

<span data-ttu-id="93bfa-324">指定したラベル ID のラベル ファイル ID を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-324">A string that indicates the label file ID for a specified label ID.</span></span>

### <a name="remarks---moduleid"></a><span data-ttu-id="93bfa-325">備考 - moduleId</span><span class="sxs-lookup"><span data-stu-id="93bfa-325">Remarks - moduleId</span></span>

<span data-ttu-id="93bfa-326">SearchFirst または searchNext のメソッドを呼び出すパラメーターとして戻り値を labelId メソッドに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-326">You need to call the searchFirst or searchNext method, and then pass the return value as a parameter to the labelId method.</span></span>

## <a name="method-morelabelfiles"></a><span data-ttu-id="93bfa-327">メソッド moreLabelFiles</span><span class="sxs-lookup"><span data-stu-id="93bfa-327">Method moreLabelFiles</span></span>

<span data-ttu-id="93bfa-328">追加のラベル ファイルがあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-328">Indicates whether there are additional label files.</span></span>

```xpp
public boolean moreLabelFiles()
```

### <a name="return-value---morelabelfiles"></a><span data-ttu-id="93bfa-329">戻り値 - moreLabelFiles</span><span class="sxs-lookup"><span data-stu-id="93bfa-329">Return Value - moreLabelFiles</span></span>

<span data-ttu-id="93bfa-330">追加のラベル ファイルがある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="93bfa-330">true if there are additional label files; otherwise, false.</span></span>

## <a name="method-name"></a><span data-ttu-id="93bfa-331">メソッド名</span><span class="sxs-lookup"><span data-stu-id="93bfa-331">Method name</span></span>

<span data-ttu-id="93bfa-332">指定したラベル ファイル ID およびラベル ID 番号に基づいて、ラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-332">Returns a label ID, based on a specified label file ID and label ID number.</span></span>

```xpp
public str name(str module, int labelId)
```

### <a name="parameters---name"></a><span data-ttu-id="93bfa-333">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="93bfa-333">Parameters - name</span></span>

<span data-ttu-id="93bfa-334">モジュール</span><span class="sxs-lookup"><span data-stu-id="93bfa-334">module</span></span>  
<span data-ttu-id="93bfa-335">ラベル ID の数値部分を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="93bfa-335">An integer that specifies the numeric part of a label ID.</span></span>

<!-- -->

<span data-ttu-id="93bfa-336">labelId</span><span class="sxs-lookup"><span data-stu-id="93bfa-336">labelId</span></span>  
<span data-ttu-id="93bfa-337">ラベル ID の数値部分を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="93bfa-337">An integer that specifies the numeric part of a label ID.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="93bfa-338">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="93bfa-338">Return Value - name</span></span>

<span data-ttu-id="93bfa-339">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-339">A string value that indicates the label ID.</span></span>

## <a name="method-searchfirst"></a><span data-ttu-id="93bfa-340">メソッド searchFirst</span><span class="sxs-lookup"><span data-stu-id="93bfa-340">Method searchFirst</span></span>

<span data-ttu-id="93bfa-341">指定した検索用語で検出された最初のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-341">Returns the first label ID that is found for a specified search term.</span></span>

```xpp
public str searchFirst(str searchString)
```

### <a name="parameters---searchfirst"></a><span data-ttu-id="93bfa-342">パラメーター - searchFirst</span><span class="sxs-lookup"><span data-stu-id="93bfa-342">Parameters - searchFirst</span></span>

<span data-ttu-id="93bfa-343">searchString</span><span class="sxs-lookup"><span data-stu-id="93bfa-343">searchString</span></span>  
<span data-ttu-id="93bfa-344">検索用語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-344">A string that specifies the search term.</span></span>

### <a name="return-value---searchfirst"></a><span data-ttu-id="93bfa-345">戻り値 - searchFirst</span><span class="sxs-lookup"><span data-stu-id="93bfa-345">Return Value - searchFirst</span></span>

<span data-ttu-id="93bfa-346">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-346">A string value that indicates the label ID.</span></span>

## <a name="method-searchnext"></a><span data-ttu-id="93bfa-347">メソッド searchNext</span><span class="sxs-lookup"><span data-stu-id="93bfa-347">Method searchNext</span></span>

<span data-ttu-id="93bfa-348">searchFirst メソッドに渡される検索用語のある次のラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-348">Returns the next label ID that is found for a search term that is passed to the searchFirst method.</span></span>

```xpp
public str searchNext()
```

### <a name="return-value---searchnext"></a><span data-ttu-id="93bfa-349">戻り値 - searchNext</span><span class="sxs-lookup"><span data-stu-id="93bfa-349">Return Value - searchNext</span></span>

<span data-ttu-id="93bfa-350">ラベル ID を示す文字列値。</span><span class="sxs-lookup"><span data-stu-id="93bfa-350">A string value that indicates the label ID.</span></span>

### <a name="remarks---searchnext"></a><span data-ttu-id="93bfa-351">備考 - searchNext</span><span class="sxs-lookup"><span data-stu-id="93bfa-351">Remarks - searchNext</span></span>

<span data-ttu-id="93bfa-352">このメソッドを呼び出す前に、searchFirst メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93bfa-352">You must call the searchFirst method before you call this method.</span></span> <span data-ttu-id="93bfa-353">それ以外の場合、このメソッドは、ランダムなラベル ID を返します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-353">Otherwise, this method returns a random label ID.</span></span>

## <a name="method-flush"></a><span data-ttu-id="93bfa-354">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="93bfa-354">Method flush</span></span>

<span data-ttu-id="93bfa-355">ディスクにラベル ファイル バッファーをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="93bfa-355">Flushes the label file buffers to disk.</span></span>

```xpp
public static boolean flush(str labelFileId, str language)
```

### <a name="parameters---flush"></a><span data-ttu-id="93bfa-356">パラメーター - flush</span><span class="sxs-lookup"><span data-stu-id="93bfa-356">Parameters - flush</span></span>

<span data-ttu-id="93bfa-357">labelFileId</span><span class="sxs-lookup"><span data-stu-id="93bfa-357">labelFileId</span></span>  
<span data-ttu-id="93bfa-358">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-358">A string that specifies a language by using a language prefix.</span></span>

<!-- -->

<span data-ttu-id="93bfa-359">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-359">language</span></span>  
<span data-ttu-id="93bfa-360">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-360">A string that specifies a language by using a language prefix.</span></span>

### <a name="return-value---flush"></a><span data-ttu-id="93bfa-361">戻り値 - flush</span><span class="sxs-lookup"><span data-stu-id="93bfa-361">Return Value - flush</span></span>

## <a name="method-new"></a><span data-ttu-id="93bfa-362">メソッド new</span><span class="sxs-lookup"><span data-stu-id="93bfa-362">Method new</span></span>

<span data-ttu-id="93bfa-363">ラベル クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="93bfa-363">Creates a new instance of the Label class.</span></span>

```xpp
public void new([str language])
```

### <a name="parameters---new"></a><span data-ttu-id="93bfa-364">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="93bfa-364">Parameters - new</span></span>

<span data-ttu-id="93bfa-365">言語</span><span class="sxs-lookup"><span data-stu-id="93bfa-365">language</span></span>  
<span data-ttu-id="93bfa-366">言語の接頭語を使用して、言語を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="93bfa-366">A string that specifies a language by using a language prefix.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="93bfa-367">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="93bfa-367">Method finalize</span></span>

<span data-ttu-id="93bfa-368">現在のラベル ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="93bfa-368">Closes the current label file.</span></span>

```xpp
public void finalize()
```

