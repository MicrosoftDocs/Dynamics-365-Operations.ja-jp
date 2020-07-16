---
title: webStaticFileNode クラス
description: このトピックでは、webStaticFileNode クラスについて説明します。
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
ms.openlocfilehash: b67944ac6411bcd72b1337bcf80729f48fe16005
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502996"
---
# <a name="class-webstaticfilenode"></a><span data-ttu-id="4e473-103">クラス webStaticFileNode</span><span class="sxs-lookup"><span data-stu-id="4e473-103">Class webStaticFileNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class webStaticFileNode extends TreeNode
```

<span data-ttu-id="4e473-104">webStaticFileNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4e473-104">The webStaticFileNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e473-105">備考</span><span class="sxs-lookup"><span data-stu-id="4e473-105">Remarks</span></span>

<span data-ttu-id="4e473-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4e473-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="4e473-107">例</span><span class="sxs-lookup"><span data-stu-id="4e473-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4e473-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="4e473-108">Methods</span></span>

| <span data-ttu-id="4e473-109">方法</span><span class="sxs-lookup"><span data-stu-id="4e473-109">Method</span></span>                                                     | <span data-ttu-id="4e473-110">説明</span><span class="sxs-lookup"><span data-stu-id="4e473-110">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e473-111">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="4e473-111">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="4e473-112">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e473-112">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="4e473-113">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-113">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="4e473-114">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-114">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="4e473-115">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-115">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="4e473-116">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-116">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="4e473-117">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-117">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="4e473-118">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-118">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="4e473-119">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-119">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="4e473-120">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-120">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="4e473-121">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-121">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="4e473-122">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-122">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="4e473-123">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-123">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="4e473-124">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-124">public str filename(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="4e473-125">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-125">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="4e473-126">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-126">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="4e473-127">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-127">public str name(\[str value\])</span></span>                             | <span data-ttu-id="4e473-128">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-128">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="4e473-129">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-129">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="4e473-130">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-130">public str relativePath(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="4e473-131">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4e473-131">public str version(\[str value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="4e473-132">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="4e473-132">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="4e473-133">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-133">Sets the source of the static file node to the given string.</span></span>                                                                              |

## <a name="method-aotgetsource"></a><span data-ttu-id="4e473-134">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-134">Method AOTgetSource</span></span>

<span data-ttu-id="4e473-135">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="4e473-135">Gets the source of the node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="4e473-136">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-136">Return Value - AOTgetSource</span></span>

<span data-ttu-id="4e473-137">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="4e473-137">The source of the node.</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="4e473-138">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-138">Remarks - AOTgetSource</span></span>

<span data-ttu-id="4e473-139">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="4e473-139">This function is overridden by nodes that have source code.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="4e473-140">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="4e473-140">Method changedBy</span></span>

<span data-ttu-id="4e473-141">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-141">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="4e473-142">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="4e473-142">Parameters - changedBy</span></span>

<span data-ttu-id="4e473-143">値</span><span class="sxs-lookup"><span data-stu-id="4e473-143">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="4e473-144">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="4e473-144">Return Value - changedBy</span></span>

<span data-ttu-id="4e473-145">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="4e473-145">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="4e473-146">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="4e473-146">Method changedDate</span></span>

<span data-ttu-id="4e473-147">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-147">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="4e473-148">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="4e473-148">Parameters - changedDate</span></span>

<span data-ttu-id="4e473-149">値</span><span class="sxs-lookup"><span data-stu-id="4e473-149">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="4e473-150">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="4e473-150">Return Value - changedDate</span></span>

<span data-ttu-id="4e473-151">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="4e473-151">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="4e473-152">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="4e473-152">Method changedTime</span></span>

<span data-ttu-id="4e473-153">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-153">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="4e473-154">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="4e473-154">Parameters - changedTime</span></span>

<span data-ttu-id="4e473-155">値</span><span class="sxs-lookup"><span data-stu-id="4e473-155">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="4e473-156">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="4e473-156">Return Value - changedTime</span></span>

<span data-ttu-id="4e473-157">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="4e473-157">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="4e473-158">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="4e473-158">Method createdBy</span></span>

<span data-ttu-id="4e473-159">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-159">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="4e473-160">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="4e473-160">Parameters - createdBy</span></span>

<span data-ttu-id="4e473-161">値</span><span class="sxs-lookup"><span data-stu-id="4e473-161">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="4e473-162">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="4e473-162">Return Value - createdBy</span></span>

<span data-ttu-id="4e473-163">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="4e473-163">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="4e473-164">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="4e473-164">Method creationDate</span></span>

<span data-ttu-id="4e473-165">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-165">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="4e473-166">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="4e473-166">Parameters - creationDate</span></span>

<span data-ttu-id="4e473-167">値</span><span class="sxs-lookup"><span data-stu-id="4e473-167">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="4e473-168">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="4e473-168">Return Value - creationDate</span></span>

<span data-ttu-id="4e473-169">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="4e473-169">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="4e473-170">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="4e473-170">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="4e473-171">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="4e473-171">Parameters - creationTime</span></span>

<span data-ttu-id="4e473-172">値</span><span class="sxs-lookup"><span data-stu-id="4e473-172">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="4e473-173">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="4e473-173">Return Value - creationTime</span></span>

## <a name="method-filename"></a><span data-ttu-id="4e473-174">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="4e473-174">Method filename</span></span>

```xpp
public str filename([str value])
```

### <a name="parameters---filename"></a><span data-ttu-id="4e473-175">パラメーター - filename</span><span class="sxs-lookup"><span data-stu-id="4e473-175">Parameters - filename</span></span>

<span data-ttu-id="4e473-176">値</span><span class="sxs-lookup"><span data-stu-id="4e473-176">value</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="4e473-177">戻り値 - filename</span><span class="sxs-lookup"><span data-stu-id="4e473-177">Return Value - filename</span></span>

## <a name="method-helptext"></a><span data-ttu-id="4e473-178">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="4e473-178">Method helpText</span></span>

<span data-ttu-id="4e473-179">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-179">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="4e473-180">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="4e473-180">Parameters - helpText</span></span>

<span data-ttu-id="4e473-181">値</span><span class="sxs-lookup"><span data-stu-id="4e473-181">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="4e473-182">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="4e473-182">Return Value - helpText</span></span>

<span data-ttu-id="4e473-183">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="4e473-183">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="4e473-184">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="4e473-184">Remarks - helpText</span></span>

<span data-ttu-id="4e473-185">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-185">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="4e473-186">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="4e473-186">The help text must not exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="4e473-187">メソッド名</span><span class="sxs-lookup"><span data-stu-id="4e473-187">Method name</span></span>

<span data-ttu-id="4e473-188">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-188">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="4e473-189">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="4e473-189">Parameters - name</span></span>

<span data-ttu-id="4e473-190">値</span><span class="sxs-lookup"><span data-stu-id="4e473-190">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="4e473-191">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="4e473-191">Return Value - name</span></span>

<span data-ttu-id="4e473-192">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="4e473-192">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="4e473-193">備考 - name</span><span class="sxs-lookup"><span data-stu-id="4e473-193">Remarks - name</span></span>

<span data-ttu-id="4e473-194">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e473-194">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="4e473-195">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="4e473-195">Begins with a letter.</span></span>
-   <span data-ttu-id="4e473-196">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="4e473-196">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="4e473-197">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4e473-197">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="4e473-198">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4e473-198">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="4e473-199">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4e473-199">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="4e473-200">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="4e473-200">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="4e473-201">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="4e473-201">Parameters - origin</span></span>

<span data-ttu-id="4e473-202">値</span><span class="sxs-lookup"><span data-stu-id="4e473-202">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="4e473-203">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="4e473-203">Return Value - origin</span></span>

## <a name="method-relativepath"></a><span data-ttu-id="4e473-204">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="4e473-204">Method relativePath</span></span>

```xpp
public str relativePath([str value])
```

### <a name="parameters---relativepath"></a><span data-ttu-id="4e473-205">パラメーター - relativePath</span><span class="sxs-lookup"><span data-stu-id="4e473-205">Parameters - relativePath</span></span>

<span data-ttu-id="4e473-206">値</span><span class="sxs-lookup"><span data-stu-id="4e473-206">value</span></span>  

### <a name="return-value---relativepath"></a><span data-ttu-id="4e473-207">戻り値 - relativePath</span><span class="sxs-lookup"><span data-stu-id="4e473-207">Return Value - relativePath</span></span>

## <a name="method-version"></a><span data-ttu-id="4e473-208">メソッド version</span><span class="sxs-lookup"><span data-stu-id="4e473-208">Method version</span></span>

```xpp
public str version([str value])
```

### <a name="parameters---version"></a><span data-ttu-id="4e473-209">パラメーター - version</span><span class="sxs-lookup"><span data-stu-id="4e473-209">Parameters - version</span></span>

<span data-ttu-id="4e473-210">値</span><span class="sxs-lookup"><span data-stu-id="4e473-210">value</span></span>  

### <a name="return-value---version"></a><span data-ttu-id="4e473-211">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="4e473-211">Return Value - version</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="4e473-212">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-212">Method AOTsetSource</span></span>

<span data-ttu-id="4e473-213">指定した文字列に静的ファイル ノードのソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="4e473-213">Sets the source of the static file node to the given string.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="4e473-214">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-214">Parameters - AOTsetSource</span></span>

<span data-ttu-id="4e473-215">ソース</span><span class="sxs-lookup"><span data-stu-id="4e473-215">source</span></span>  
<span data-ttu-id="4e473-216">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="4e473-216">An optional parameter that marks whether the source that is provided is static.</span></span>

<!-- -->

<span data-ttu-id="4e473-217">isStatic</span><span class="sxs-lookup"><span data-stu-id="4e473-217">isStatic</span></span>  
<span data-ttu-id="4e473-218">提供されるソースが静的であるかどうかを示すオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="4e473-218">An optional parameter that marks whether the source that is provided is static.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="4e473-219">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="4e473-219">Remarks - AOTsetSource</span></span>

<span data-ttu-id="4e473-220">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="4e473-220">This method is overridden by nodes that have source code.</span></span>

