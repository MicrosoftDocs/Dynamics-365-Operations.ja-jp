---
title: Job クラス
description: このトピックでは、Job クラスについて説明します。
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
ms.openlocfilehash: e73a68e3243da4ac17a8f97985d56f9a754e1145
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502593"
---
# <a name="class-job"></a><span data-ttu-id="cc452-103">クラス ジョブ</span><span class="sxs-lookup"><span data-stu-id="cc452-103">Class Job</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Job extends TreeNode
```

<span data-ttu-id="cc452-104">Job クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cc452-104">The Job class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc452-105">備考</span><span class="sxs-lookup"><span data-stu-id="cc452-105">Remarks</span></span>

<span data-ttu-id="cc452-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cc452-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="cc452-107">例</span><span class="sxs-lookup"><span data-stu-id="cc452-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="cc452-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc452-108">Methods</span></span>

| <span data-ttu-id="cc452-109">方法</span><span class="sxs-lookup"><span data-stu-id="cc452-109">Method</span></span>                                                     | <span data-ttu-id="cc452-110">説明</span><span class="sxs-lookup"><span data-stu-id="cc452-110">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc452-111">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="cc452-111">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="cc452-112">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="cc452-112">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="cc452-113">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-113">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="cc452-114">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-114">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="cc452-115">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-115">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="cc452-116">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-116">Gets or sets the date that an application object was last changed.</span></span>                                                                            |
| <span data-ttu-id="cc452-117">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-117">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="cc452-118">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-118">Gets or sets the time that an application object was last changed.</span></span>                                                                            |
| <span data-ttu-id="cc452-119">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-119">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="cc452-120">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-120">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="cc452-121">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-121">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="cc452-122">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-122">Gets or sets the date that an application object was created.</span></span>                                                                                 |
| <span data-ttu-id="cc452-123">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-123">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="cc452-124">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-124">public str name(\[str value\])</span></span>                             | <span data-ttu-id="cc452-125">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-125">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="cc452-126">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="cc452-126">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="cc452-127">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="cc452-127">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="cc452-128">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-128">Sets the source code of this node.</span></span>                                                                                                            |
| <span data-ttu-id="cc452-129">public void AOTrun()</span><span class="sxs-lookup"><span data-stu-id="cc452-129">public void AOTrun()</span></span>                                       | <span data-ttu-id="cc452-130">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="cc452-130">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>                                                |
| <span data-ttu-id="cc452-131">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="cc452-131">public void AOTedit(\[int Line\], \[int Column\])</span></span>          | <span data-ttu-id="cc452-132">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc452-132">Opens the appropriate editor for this node.</span></span>                                                                                                   |

## <a name="method-aotgetsource"></a><span data-ttu-id="cc452-133">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="cc452-133">Method AOTgetSource</span></span>

<span data-ttu-id="cc452-134">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="cc452-134">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="cc452-135">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="cc452-135">Return Value - AOTgetSource</span></span>

<span data-ttu-id="cc452-136">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null を参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="cc452-136">A string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="cc452-137">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="cc452-137">Remarks - AOTgetSource</span></span>

<span data-ttu-id="cc452-138">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="cc452-138">This function is overridden by nodes that have source code.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="cc452-139">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="cc452-139">Method changedBy</span></span>

<span data-ttu-id="cc452-140">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-140">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="cc452-141">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="cc452-141">Parameters - changedBy</span></span>

<span data-ttu-id="cc452-142">値</span><span class="sxs-lookup"><span data-stu-id="cc452-142">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="cc452-143">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="cc452-143">Return Value - changedBy</span></span>

<span data-ttu-id="cc452-144">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="cc452-144">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="cc452-145">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="cc452-145">Method changedDate</span></span>

<span data-ttu-id="cc452-146">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-146">Gets or sets the date that an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="cc452-147">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="cc452-147">Parameters - changedDate</span></span>

<span data-ttu-id="cc452-148">値</span><span class="sxs-lookup"><span data-stu-id="cc452-148">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="cc452-149">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="cc452-149">Return Value - changedDate</span></span>

<span data-ttu-id="cc452-150">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="cc452-150">The date that an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="cc452-151">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="cc452-151">Method changedTime</span></span>

<span data-ttu-id="cc452-152">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-152">Gets or sets the time that an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="cc452-153">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="cc452-153">Parameters - changedTime</span></span>

<span data-ttu-id="cc452-154">値</span><span class="sxs-lookup"><span data-stu-id="cc452-154">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="cc452-155">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="cc452-155">Return Value - changedTime</span></span>

<span data-ttu-id="cc452-156">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="cc452-156">The time that an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="cc452-157">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="cc452-157">Method createdBy</span></span>

<span data-ttu-id="cc452-158">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-158">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="cc452-159">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="cc452-159">Parameters - createdBy</span></span>

<span data-ttu-id="cc452-160">値</span><span class="sxs-lookup"><span data-stu-id="cc452-160">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="cc452-161">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="cc452-161">Return Value - createdBy</span></span>

<span data-ttu-id="cc452-162">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="cc452-162">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="cc452-163">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="cc452-163">Method creationDate</span></span>

<span data-ttu-id="cc452-164">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-164">Gets or sets the date that an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="cc452-165">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="cc452-165">Parameters - creationDate</span></span>

<span data-ttu-id="cc452-166">値</span><span class="sxs-lookup"><span data-stu-id="cc452-166">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="cc452-167">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="cc452-167">Return Value - creationDate</span></span>

<span data-ttu-id="cc452-168">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="cc452-168">The date that an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="cc452-169">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="cc452-169">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="cc452-170">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="cc452-170">Parameters - creationTime</span></span>

<span data-ttu-id="cc452-171">値</span><span class="sxs-lookup"><span data-stu-id="cc452-171">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="cc452-172">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="cc452-172">Return Value - creationTime</span></span>

## <a name="method-name"></a><span data-ttu-id="cc452-173">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cc452-173">Method name</span></span>

<span data-ttu-id="cc452-174">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-174">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="cc452-175">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="cc452-175">Parameters - name</span></span>

<span data-ttu-id="cc452-176">値</span><span class="sxs-lookup"><span data-stu-id="cc452-176">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="cc452-177">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="cc452-177">Return Value - name</span></span>

<span data-ttu-id="cc452-178">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="cc452-178">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="cc452-179">備考 - name</span><span class="sxs-lookup"><span data-stu-id="cc452-179">Remarks - name</span></span>

<span data-ttu-id="cc452-180">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc452-180">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="cc452-181">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="cc452-181">Begins with a letter.</span></span>
-   <span data-ttu-id="cc452-182">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="cc452-182">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="cc452-183">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cc452-183">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="cc452-184">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="cc452-184">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="cc452-185">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="cc452-185">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="cc452-186">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="cc452-186">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="cc452-187">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="cc452-187">Parameters - origin</span></span>

<span data-ttu-id="cc452-188">値</span><span class="sxs-lookup"><span data-stu-id="cc452-188">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="cc452-189">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="cc452-189">Return Value - origin</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="cc452-190">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="cc452-190">Method AOTsetSource</span></span>

<span data-ttu-id="cc452-191">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="cc452-191">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="cc452-192">パラメーター - AOTsetSource </span><span class="sxs-lookup"><span data-stu-id="cc452-192">Parameters - AOTsetSource</span></span>

<span data-ttu-id="cc452-193">ソース</span><span class="sxs-lookup"><span data-stu-id="cc452-193">source</span></span>  
<span data-ttu-id="cc452-194">メソッドが静的かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="cc452-194">A value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="cc452-195">isStatic</span><span class="sxs-lookup"><span data-stu-id="cc452-195">isStatic</span></span>  
<span data-ttu-id="cc452-196">メソッドが静的かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="cc452-196">A value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="cc452-197">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="cc452-197">Remarks - AOTsetSource</span></span>

<span data-ttu-id="cc452-198">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="cc452-198">This method is overridden by nodes that have source code.</span></span>

## <a name="method-aotrun"></a><span data-ttu-id="cc452-199">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="cc452-199">Method AOTrun</span></span>

<span data-ttu-id="cc452-200">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="cc452-200">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>

```xpp
public void AOTrun()
```

## <a name="method-aotedit"></a><span data-ttu-id="cc452-201">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="cc452-201">Method AOTedit</span></span>

<span data-ttu-id="cc452-202">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc452-202">Opens the appropriate editor for this node.</span></span>

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a><span data-ttu-id="cc452-203">パラメーター - AOTedit</span><span class="sxs-lookup"><span data-stu-id="cc452-203">Parameters - AOTedit</span></span>

<span data-ttu-id="cc452-204">折れ線</span><span class="sxs-lookup"><span data-stu-id="cc452-204">Line</span></span>  
<span data-ttu-id="cc452-205">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="cc452-205">The column of the cursor position; optional.</span></span>

<!-- -->

<span data-ttu-id="cc452-206">円柱</span><span class="sxs-lookup"><span data-stu-id="cc452-206">Column</span></span>  
<span data-ttu-id="cc452-207">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="cc452-207">The column of the cursor position; optional.</span></span>

### <a name="remarks---aotedit"></a><span data-ttu-id="cc452-208">備考 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="cc452-208">Remarks - AOTedit</span></span>

<span data-ttu-id="cc452-209">ノードがメソッドである場合は、コード エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="cc452-209">If the node is a method, the code editor opens.</span></span> <span data-ttu-id="cc452-210">ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="cc452-210">If the node is a documentation object, the Help editor opens.</span></span>


