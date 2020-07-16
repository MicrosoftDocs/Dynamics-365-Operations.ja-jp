---
title: webListDefNode クラス
description: このトピックでは、webListDefNode クラスについて説明します。
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
ms.openlocfilehash: 7fe0ffc321dc1a0548d9cb1ed2dc2b53def974aa
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502997"
---
# <a name="class-weblistdefnode"></a><span data-ttu-id="96719-103">クラス webListDefNode</span><span class="sxs-lookup"><span data-stu-id="96719-103">Class webListDefNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class webListDefNode extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="96719-104">備考</span><span class="sxs-lookup"><span data-stu-id="96719-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="96719-105">例</span><span class="sxs-lookup"><span data-stu-id="96719-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="96719-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="96719-106">Methods</span></span>

| <span data-ttu-id="96719-107">方法</span><span class="sxs-lookup"><span data-stu-id="96719-107">Method</span></span>                                                     | <span data-ttu-id="96719-108">説明</span><span class="sxs-lookup"><span data-stu-id="96719-108">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96719-109">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="96719-109">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="96719-110">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="96719-110">Returns the source code of this node.</span></span>                                                                                                     |
| <span data-ttu-id="96719-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-111">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="96719-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="96719-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="96719-113">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="96719-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-114">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="96719-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-115">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="96719-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-116">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="96719-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-117">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="96719-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-118">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="96719-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="96719-119">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="96719-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-120">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="96719-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-121">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="96719-122">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-122">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="96719-123">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-123">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="96719-124">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="96719-124">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="96719-125">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-125">public str name(\[str value\])</span></span>                             | <span data-ttu-id="96719-126">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-126">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="96719-127">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="96719-127">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="96719-128">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-128">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="96719-129">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="96719-129">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="96719-130">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-130">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="96719-131">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="96719-131">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="96719-132">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="96719-132">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="96719-133">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-133">Sets the source code of this node.</span></span>                                                                                                        |
| <span data-ttu-id="96719-134">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="96719-134">public void new(str name)</span></span>                                  | <span data-ttu-id="96719-135">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="96719-135">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

## <a name="method-aotgetsource"></a><span data-ttu-id="96719-136">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="96719-136">Method AOTgetSource</span></span>

<span data-ttu-id="96719-137">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="96719-137">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="96719-138">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="96719-138">Return Value - AOTgetSource</span></span>

<span data-ttu-id="96719-139">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="96719-139">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="96719-140">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="96719-140">Remarks - AOTgetSource</span></span>

<span data-ttu-id="96719-141">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="96719-141">This function is overridden by nodes that have source code.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="96719-142">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="96719-142">Method changedBy</span></span>

<span data-ttu-id="96719-143">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-143">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="96719-144">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="96719-144">Parameters - changedBy</span></span>

<span data-ttu-id="96719-145">値</span><span class="sxs-lookup"><span data-stu-id="96719-145">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="96719-146">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="96719-146">Return Value - changedBy</span></span>

<span data-ttu-id="96719-147">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="96719-147">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="96719-148">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="96719-148">Method changedDate</span></span>

<span data-ttu-id="96719-149">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-149">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="96719-150">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="96719-150">Parameters - changedDate</span></span>

<span data-ttu-id="96719-151">値</span><span class="sxs-lookup"><span data-stu-id="96719-151">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="96719-152">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="96719-152">Return Value - changedDate</span></span>

<span data-ttu-id="96719-153">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="96719-153">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="96719-154">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="96719-154">Method changedTime</span></span>

<span data-ttu-id="96719-155">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-155">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="96719-156">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="96719-156">Parameters - changedTime</span></span>

<span data-ttu-id="96719-157">値</span><span class="sxs-lookup"><span data-stu-id="96719-157">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="96719-158">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="96719-158">Return Value - changedTime</span></span>

<span data-ttu-id="96719-159">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="96719-159">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="96719-160">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="96719-160">Method createdBy</span></span>

<span data-ttu-id="96719-161">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-161">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="96719-162">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="96719-162">Parameters - createdBy</span></span>

<span data-ttu-id="96719-163">値</span><span class="sxs-lookup"><span data-stu-id="96719-163">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="96719-164">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="96719-164">Return Value - createdBy</span></span>

<span data-ttu-id="96719-165">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="96719-165">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="96719-166">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="96719-166">Method creationDate</span></span>

<span data-ttu-id="96719-167">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-167">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="96719-168">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="96719-168">Parameters - creationDate</span></span>

<span data-ttu-id="96719-169">値</span><span class="sxs-lookup"><span data-stu-id="96719-169">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="96719-170">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="96719-170">Return Value - creationDate</span></span>

<span data-ttu-id="96719-171">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="96719-171">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="96719-172">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="96719-172">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="96719-173">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="96719-173">Parameters - creationTime</span></span>

<span data-ttu-id="96719-174">値</span><span class="sxs-lookup"><span data-stu-id="96719-174">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="96719-175">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="96719-175">Return Value - creationTime</span></span>

## <a name="method-helptext"></a><span data-ttu-id="96719-176">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="96719-176">Method helpText</span></span>

<span data-ttu-id="96719-177">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-177">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="96719-178">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="96719-178">Parameters - helpText</span></span>

<span data-ttu-id="96719-179">値</span><span class="sxs-lookup"><span data-stu-id="96719-179">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="96719-180">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="96719-180">Return Value - helpText</span></span>

<span data-ttu-id="96719-181">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="96719-181">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="96719-182">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="96719-182">Remarks - helpText</span></span>

<span data-ttu-id="96719-183">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-183">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="96719-184">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="96719-184">The help text must not exceed 250 characters.</span></span>

## <a name="method-mossonly"></a><span data-ttu-id="96719-185">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="96719-185">Method mOSSOnly</span></span>

```xpp
public boolean mOSSOnly([boolean value])
```

### <a name="parameters---mossonly"></a><span data-ttu-id="96719-186">パラメーター - mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="96719-186">Parameters - mOSSOnly</span></span>

<span data-ttu-id="96719-187">値</span><span class="sxs-lookup"><span data-stu-id="96719-187">value</span></span>  

### <a name="return-value---mossonly"></a><span data-ttu-id="96719-188">戻り値 - mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="96719-188">Return Value - mOSSOnly</span></span>

## <a name="method-name"></a><span data-ttu-id="96719-189">メソッド名</span><span class="sxs-lookup"><span data-stu-id="96719-189">Method name</span></span>

<span data-ttu-id="96719-190">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-190">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="96719-191">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="96719-191">Parameters - name</span></span>

<span data-ttu-id="96719-192">値</span><span class="sxs-lookup"><span data-stu-id="96719-192">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="96719-193">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="96719-193">Return Value - name</span></span>

<span data-ttu-id="96719-194">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="96719-194">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="96719-195">備考 - name</span><span class="sxs-lookup"><span data-stu-id="96719-195">Remarks - name</span></span>

<span data-ttu-id="96719-196">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="96719-196">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="96719-197">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="96719-197">Begins with a letter.</span></span>
-   <span data-ttu-id="96719-198">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="96719-198">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="96719-199">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="96719-199">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="96719-200">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="96719-200">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="96719-201">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="96719-201">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="96719-202">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="96719-202">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="96719-203">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="96719-203">Parameters - origin</span></span>

<span data-ttu-id="96719-204">値</span><span class="sxs-lookup"><span data-stu-id="96719-204">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="96719-205">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="96719-205">Return Value - origin</span></span>

## <a name="method-pagetitle"></a><span data-ttu-id="96719-206">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="96719-206">Method pageTitle</span></span>

```xpp
public str pageTitle([str value])
```

### <a name="parameters---pagetitle"></a><span data-ttu-id="96719-207">パラメーター - pageTitle</span><span class="sxs-lookup"><span data-stu-id="96719-207">Parameters - pageTitle</span></span>

<span data-ttu-id="96719-208">値</span><span class="sxs-lookup"><span data-stu-id="96719-208">value</span></span>  

### <a name="return-value---pagetitle"></a><span data-ttu-id="96719-209">戻り値 - pageTitle</span><span class="sxs-lookup"><span data-stu-id="96719-209">Return Value - pageTitle</span></span>

## <a name="method-publicpage"></a><span data-ttu-id="96719-210">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="96719-210">Method publicPage</span></span>

```xpp
public boolean publicPage([boolean value])
```

### <a name="parameters---publicpage"></a><span data-ttu-id="96719-211">パラメーター - publicPage</span><span class="sxs-lookup"><span data-stu-id="96719-211">Parameters - publicPage</span></span>

<span data-ttu-id="96719-212">値</span><span class="sxs-lookup"><span data-stu-id="96719-212">value</span></span>  

### <a name="return-value---publicpage"></a><span data-ttu-id="96719-213">戻り値 - publicPage</span><span class="sxs-lookup"><span data-stu-id="96719-213">Return Value - publicPage</span></span>

## <a name="method-url"></a><span data-ttu-id="96719-214">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="96719-214">Method uRL</span></span>

```xpp
public str uRL([str value])
```

### <a name="parameters---url"></a><span data-ttu-id="96719-215">パラメーター - uRL</span><span class="sxs-lookup"><span data-stu-id="96719-215">Parameters - uRL</span></span>

<span data-ttu-id="96719-216">値</span><span class="sxs-lookup"><span data-stu-id="96719-216">value</span></span>  

### <a name="return-value---url"></a><span data-ttu-id="96719-217">戻り値 - uRL</span><span class="sxs-lookup"><span data-stu-id="96719-217">Return Value - uRL</span></span>

## <a name="method-webmodule"></a><span data-ttu-id="96719-218">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="96719-218">Method webModule</span></span>

```xpp
public str webModule([str value])
```

### <a name="parameters---webmodule"></a><span data-ttu-id="96719-219">パラメーター - webModule</span><span class="sxs-lookup"><span data-stu-id="96719-219">Parameters - webModule</span></span>

<span data-ttu-id="96719-220">値</span><span class="sxs-lookup"><span data-stu-id="96719-220">value</span></span>  

### <a name="return-value---webmodule"></a><span data-ttu-id="96719-221">戻り値 - webModule</span><span class="sxs-lookup"><span data-stu-id="96719-221">Return Value - webModule</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="96719-222">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="96719-222">Method AOTsetSource</span></span>

<span data-ttu-id="96719-223">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="96719-223">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="96719-224">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="96719-224">Parameters - AOTsetSource</span></span>

<span data-ttu-id="96719-225">ソース</span><span class="sxs-lookup"><span data-stu-id="96719-225">source</span></span>  
<span data-ttu-id="96719-226">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="96719-226">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="96719-227">isStatic</span><span class="sxs-lookup"><span data-stu-id="96719-227">isStatic</span></span>  
<span data-ttu-id="96719-228">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="96719-228">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="96719-229">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="96719-229">Remarks - AOTsetSource</span></span>

<span data-ttu-id="96719-230">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="96719-230">This method is overridden by nodes that have source code.</span></span>

## <a name="method-new"></a><span data-ttu-id="96719-231">メソッド new</span><span class="sxs-lookup"><span data-stu-id="96719-231">Method new</span></span>

<span data-ttu-id="96719-232">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="96719-232">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="96719-233">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="96719-233">Parameters - new</span></span>

<span data-ttu-id="96719-234">名前</span><span class="sxs-lookup"><span data-stu-id="96719-234">name</span></span>  

