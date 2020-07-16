---
title: QueryHavingFilter クラス
description: このトピックでは、QueryHavingFilter クラスについて説明します。
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
ms.openlocfilehash: 5dbbb78e39a0692044c91db8c35ad46c2946cf43
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502861"
---
# <a name="class-queryhavingfilter"></a><span data-ttu-id="f9b63-103">クラス QueryHavingFilter</span><span class="sxs-lookup"><span data-stu-id="f9b63-103">Class QueryHavingFilter</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryHavingFilter extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="f9b63-104">備考</span><span class="sxs-lookup"><span data-stu-id="f9b63-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f9b63-105">例</span><span class="sxs-lookup"><span data-stu-id="f9b63-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f9b63-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="f9b63-106">Methods</span></span>

| <span data-ttu-id="f9b63-107">方法</span><span class="sxs-lookup"><span data-stu-id="f9b63-107">Method</span></span>                                          | <span data-ttu-id="f9b63-108">説明</span><span class="sxs-lookup"><span data-stu-id="f9b63-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b63-109">public AggregateFunction aggregateFunction()</span><span class="sxs-lookup"><span data-stu-id="f9b63-109">public AggregateFunction aggregateFunction()</span></span>    |                                                                                                                                           |
| <span data-ttu-id="f9b63-110">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="f9b63-110">public QueryBuildDataSource dataSource()</span></span>        |                                                                                                                                           |
| <span data-ttu-id="f9b63-111">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-111">public boolean enabled(\[boolean value\])</span></span>       | <span data-ttu-id="f9b63-112">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-112">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="f9b63-113">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-113">public FieldId field(\[FieldId value\])</span></span>         | <span data-ttu-id="f9b63-114">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-114">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="f9b63-115">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="f9b63-115">public int fieldArrayIndex()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f9b63-116">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="f9b63-116">public FieldName fieldName()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f9b63-117">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-117">public str label(\[str value\])</span></span>                 | <span data-ttu-id="f9b63-118">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-118">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="f9b63-119">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-119">public str name(\[str value\])</span></span>                  | <span data-ttu-id="f9b63-120">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-120">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="f9b63-121">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="f9b63-121">public str prompt()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9b63-122">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-122">public int status(\[int value\])</span></span>                | <span data-ttu-id="f9b63-123">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-123">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="f9b63-124">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-124">public TableId table(\[TableId value\])</span></span>         | <span data-ttu-id="f9b63-125">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-125">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="f9b63-126">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-126">public TableId tableSelector(\[TableId value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="f9b63-127">public str toString()</span><span class="sxs-lookup"><span data-stu-id="f9b63-127">public str toString()</span></span>                           | <span data-ttu-id="f9b63-128">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-128">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="f9b63-129">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="f9b63-129">public int typeof()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9b63-130">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="f9b63-130">public boolean valid()</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="f9b63-131">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9b63-131">public str value(\[str value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="f9b63-132">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f9b63-132">public void finalize()</span></span>                          |                                                                                                                                           |

## <a name="method-aggregatefunction"></a><span data-ttu-id="f9b63-133">メソッド aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="f9b63-133">Method aggregateFunction</span></span>

```xpp
public AggregateFunction aggregateFunction()
```

### <a name="return-value---aggregatefunction"></a><span data-ttu-id="f9b63-134">戻り値 - aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="f9b63-134">Return Value - aggregateFunction</span></span>

## <a name="method-datasource"></a><span data-ttu-id="f9b63-135">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="f9b63-135">Method dataSource</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="f9b63-136">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="f9b63-136">Return Value - dataSource</span></span>

## <a name="method-enabled"></a><span data-ttu-id="f9b63-137">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="f9b63-137">Method enabled</span></span>

<span data-ttu-id="f9b63-138">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-138">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="f9b63-139">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="f9b63-139">Parameters - enabled</span></span>

<span data-ttu-id="f9b63-140">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-140">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="f9b63-141">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="f9b63-141">Return Value - enabled</span></span>

<span data-ttu-id="f9b63-142">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f9b63-142">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="f9b63-143">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="f9b63-143">Remarks - enabled</span></span>

<span data-ttu-id="f9b63-144">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-144">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="f9b63-145">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-145">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="f9b63-146">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-146">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-field"></a><span data-ttu-id="f9b63-147">メソッド field</span><span class="sxs-lookup"><span data-stu-id="f9b63-147">Method field</span></span>

<span data-ttu-id="f9b63-148">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-148">Gets or sets the field ID associated with the object.</span></span>

```xpp
public FieldId field([FieldId value])
```

### <a name="parameters---field"></a><span data-ttu-id="f9b63-149">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="f9b63-149">Parameters - field</span></span>

<span data-ttu-id="f9b63-150">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-150">value</span></span>  

### <a name="return-value---field"></a><span data-ttu-id="f9b63-151">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="f9b63-151">Return Value - field</span></span>

<span data-ttu-id="f9b63-152">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9b63-152">The current value of the field ID associated with the object.</span></span>

## <a name="method-fieldarrayindex"></a><span data-ttu-id="f9b63-153">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="f9b63-153">Method fieldArrayIndex</span></span>

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a><span data-ttu-id="f9b63-154">戻り値 - fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="f9b63-154">Return Value - fieldArrayIndex</span></span>

## <a name="method-fieldname"></a><span data-ttu-id="f9b63-155">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="f9b63-155">Method fieldName</span></span>

```xpp
public FieldName fieldName()
```

### <a name="return-value---fieldname"></a><span data-ttu-id="f9b63-156">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="f9b63-156">Return Value - fieldName</span></span>

## <a name="method-label"></a><span data-ttu-id="f9b63-157">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f9b63-157">Method label</span></span>

<span data-ttu-id="f9b63-158">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-158">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="f9b63-159">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="f9b63-159">Parameters - label</span></span>

<span data-ttu-id="f9b63-160">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-160">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="f9b63-161">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="f9b63-161">Return Value - label</span></span>

<span data-ttu-id="f9b63-162">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9b63-162">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="f9b63-163">備考 - label</span><span class="sxs-lookup"><span data-stu-id="f9b63-163">Remarks - label</span></span>

<span data-ttu-id="f9b63-164">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-164">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="f9b63-165">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f9b63-165">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="f9b63-166">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f9b63-166">Method name</span></span>

<span data-ttu-id="f9b63-167">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-167">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="f9b63-168">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="f9b63-168">Parameters - name</span></span>

<span data-ttu-id="f9b63-169">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-169">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="f9b63-170">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f9b63-170">Return Value - name</span></span>

<span data-ttu-id="f9b63-171">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f9b63-171">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="f9b63-172">備考 - name</span><span class="sxs-lookup"><span data-stu-id="f9b63-172">Remarks - name</span></span>

<span data-ttu-id="f9b63-173">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9b63-173">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f9b63-174">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-174">Begins with a letter.</span></span>
-   <span data-ttu-id="f9b63-175">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f9b63-175">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f9b63-176">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-176">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f9b63-177">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f9b63-177">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f9b63-178">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f9b63-178">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-prompt"></a><span data-ttu-id="f9b63-179">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="f9b63-179">Method prompt</span></span>

```xpp
public str prompt()
```

### <a name="return-value---prompt"></a><span data-ttu-id="f9b63-180">戻り値 - prompt</span><span class="sxs-lookup"><span data-stu-id="f9b63-180">Return Value - prompt</span></span>

## <a name="method-status"></a><span data-ttu-id="f9b63-181">メソッド status</span><span class="sxs-lookup"><span data-stu-id="f9b63-181">Method status</span></span>

<span data-ttu-id="f9b63-182">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-182">Gets or sets the status of an object.</span></span>

```xpp
public int status([int value])
```

### <a name="parameters---status"></a><span data-ttu-id="f9b63-183">パラメーター - status</span><span class="sxs-lookup"><span data-stu-id="f9b63-183">Parameters - status</span></span>

<span data-ttu-id="f9b63-184">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-184">value</span></span>  

### <a name="return-value---status"></a><span data-ttu-id="f9b63-185">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="f9b63-185">Return Value - status</span></span>

<span data-ttu-id="f9b63-186">オブジェクトのステータスの現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9b63-186">The current value of the status of the object.</span></span>

## <a name="method-table"></a><span data-ttu-id="f9b63-187">メソッド table</span><span class="sxs-lookup"><span data-stu-id="f9b63-187">Method table</span></span>

<span data-ttu-id="f9b63-188">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-188">Gets or sets the table ID that is associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="f9b63-189">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="f9b63-189">Parameters - table</span></span>

<span data-ttu-id="f9b63-190">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-190">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="f9b63-191">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="f9b63-191">Return Value - table</span></span>

<span data-ttu-id="f9b63-192">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9b63-192">The current value of the table ID that is associated with the object.</span></span>

## <a name="method-tableselector"></a><span data-ttu-id="f9b63-193">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="f9b63-193">Method tableSelector</span></span>

```xpp
public TableId tableSelector([TableId value])
```

### <a name="parameters---tableselector"></a><span data-ttu-id="f9b63-194">パラメーター - tableSelector</span><span class="sxs-lookup"><span data-stu-id="f9b63-194">Parameters - tableSelector</span></span>

<span data-ttu-id="f9b63-195">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-195">value</span></span>  

### <a name="return-value---tableselector"></a><span data-ttu-id="f9b63-196">戻り値 - tableSelector</span><span class="sxs-lookup"><span data-stu-id="f9b63-196">Return Value - tableSelector</span></span>

## <a name="method-tostring"></a><span data-ttu-id="f9b63-197">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="f9b63-197">Method toString</span></span>

<span data-ttu-id="f9b63-198">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-198">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="f9b63-199">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="f9b63-199">Return Value - toString</span></span>

<span data-ttu-id="f9b63-200">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f9b63-200">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="f9b63-201">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="f9b63-201">Remarks - toString</span></span>

<span data-ttu-id="f9b63-202">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-202">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="f9b63-203">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f9b63-203">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="f9b63-204">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f9b63-204">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-typeof"></a><span data-ttu-id="f9b63-205">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="f9b63-205">Method typeof</span></span>

```xpp
public int typeof()
```

### <a name="return-value---typeof"></a><span data-ttu-id="f9b63-206">戻り値 - typeof</span><span class="sxs-lookup"><span data-stu-id="f9b63-206">Return Value - typeof</span></span>

## <a name="method-valid"></a><span data-ttu-id="f9b63-207">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="f9b63-207">Method valid</span></span>

```xpp
public boolean valid()
```

### <a name="return-value---valid"></a><span data-ttu-id="f9b63-208">戻り値 - valid</span><span class="sxs-lookup"><span data-stu-id="f9b63-208">Return Value - valid</span></span>

## <a name="method-value"></a><span data-ttu-id="f9b63-209">メソッド value</span><span class="sxs-lookup"><span data-stu-id="f9b63-209">Method value</span></span>

```xpp
public str value([str value])
```

### <a name="parameters---value"></a><span data-ttu-id="f9b63-210">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="f9b63-210">Parameters - value</span></span>

<span data-ttu-id="f9b63-211">値</span><span class="sxs-lookup"><span data-stu-id="f9b63-211">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="f9b63-212">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="f9b63-212">Return Value - value</span></span>

## <a name="method-finalize"></a><span data-ttu-id="f9b63-213">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f9b63-213">Method finalize</span></span>

```xpp
public void finalize()
```

