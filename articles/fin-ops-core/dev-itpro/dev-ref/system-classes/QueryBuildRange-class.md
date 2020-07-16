---
title: QueryBuildRange クラス
description: このトピックでは、QueryBuildRange クラスについて説明します。
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
ms.openlocfilehash: 67068c136edd3a363afc552c2c4b701fa25c9b51
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502864"
---
# <a name="class-querybuildrange"></a><span data-ttu-id="5ae43-103">クラス QueryBuildRange</span><span class="sxs-lookup"><span data-stu-id="5ae43-103">Class QueryBuildRange</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildRange extends TreeNode
```

<span data-ttu-id="5ae43-104">QueryBuildRange クラスは、QueryBuildRange クラスが関連付けられているデータ ソースからフェッチするレコードを定義する範囲を表します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-104">The QueryBuildRange class represents the ranges that define which records should be fetched from the data source in which the QueryBuildRange class is associated.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae43-105">備考</span><span class="sxs-lookup"><span data-stu-id="5ae43-105">Remarks</span></span>

<span data-ttu-id="5ae43-106">value プロパティを使用して、範囲を定義する文字列を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-106">The value property can be used to set the string that defines the range.</span></span> <span data-ttu-id="5ae43-107">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-107">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="5ae43-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="5ae43-109">特定のデータ ソースは、任意の数の範囲を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-109">A particular data source can have any number of ranges.</span></span> <span data-ttu-id="5ae43-110">複数の範囲は、同じデータ ソース フィールドに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="5ae43-110">Multiple ranges are valid for the same data source field.</span></span>

## <a name="examples"></a><span data-ttu-id="5ae43-111">例</span><span class="sxs-lookup"><span data-stu-id="5ae43-111">Examples</span></span>

<span data-ttu-id="5ae43-112">次の基本的な例は、QueryBuildRange クラスを使用して特定のデータ フィールドの対象範囲を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5ae43-112">The following basic example shows how to use the QueryBuildRange class to specify the range of interest for a specific data field.</span></span>

```xpp
Query                   query; 
QueryRun                queryRun; 
QueryBuildDataSource    queryBuildDataSource; 
QueryBuildRange         queryBuildRange; 
CustTable               custTable; 
query = new Query(); 
queryBuildDataSource = query.addDataSource( 
   TableNum(CustTable)); 
queryBuildRange = queryBuildDataSource.addRange( 
    FieldNum(CustTable,AccountNum)); 
queryBuildRange.value("4000..5000"); 
queryRun = new queryRun(query); 
if (queryRun.prompt()) 
{ 
    while (queryRun.next()) 
    { 
        custTable = queryRun.get(TableNum(CustTable)); 
        print custTable.AccountNum; 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="5ae43-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="5ae43-113">Methods</span></span>

| <span data-ttu-id="5ae43-114">方法</span><span class="sxs-lookup"><span data-stu-id="5ae43-114">Method</span></span>                                                        | <span data-ttu-id="5ae43-115">説明</span><span class="sxs-lookup"><span data-stu-id="5ae43-115">Description</span></span>                                                                                                                               |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae43-116">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="5ae43-116">public QueryBuildDataSource dataSource()</span></span>                      | <span data-ttu-id="5ae43-117">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-117">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>                                                          |
| <span data-ttu-id="5ae43-118">public boolean doesRangeNodeBelongToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="5ae43-118">public boolean doesRangeNodeBelongToCompositeQuery()</span></span>          |                                                                                                                                           |
| <span data-ttu-id="5ae43-119">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-119">public boolean enabled(\[boolean value\])</span></span>                     | <span data-ttu-id="5ae43-120">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-120">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="5ae43-121">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-121">public FieldId field(\[FieldId value\])</span></span>                       | <span data-ttu-id="5ae43-122">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-122">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="5ae43-123">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="5ae43-123">public int fieldArrayIndex()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="5ae43-124">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="5ae43-124">public FieldName fieldName()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="5ae43-125">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-125">public str label(\[str value\])</span></span>                               | <span data-ttu-id="5ae43-126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-126">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="5ae43-127">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-127">public str name(\[str value\])</span></span>                                | <span data-ttu-id="5ae43-128">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-128">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="5ae43-129">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="5ae43-129">public str prompt()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="5ae43-130">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-130">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="5ae43-131">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-131">public int status(\[int value\])</span></span>                              | <span data-ttu-id="5ae43-132">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-132">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="5ae43-133">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-133">public TableId table(\[TableId value\])</span></span>                       | <span data-ttu-id="5ae43-134">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-134">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="5ae43-135">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-135">public TableId tableSelector(\[TableId value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="5ae43-136">public str toString()</span><span class="sxs-lookup"><span data-stu-id="5ae43-136">public str toString()</span></span>                                         | <span data-ttu-id="5ae43-137">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-137">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="5ae43-138">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="5ae43-138">public int typeof()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="5ae43-139">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="5ae43-139">public boolean valid()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="5ae43-140">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5ae43-140">public str value(\[str value\])</span></span>                               | <span data-ttu-id="5ae43-141">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-141">Gets or sets the value that queried records must match to be retrieved.</span></span>                                                                   |
| <span data-ttu-id="5ae43-142">public void associateRangeNodeToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="5ae43-142">public void associateRangeNodeToCompositeQuery()</span></span>              |                                                                                                                                           |
| <span data-ttu-id="5ae43-143">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="5ae43-143">public void finalize()</span></span>                                        |                                                                                                                                           |

## <a name="method-datasource"></a><span data-ttu-id="5ae43-144">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="5ae43-144">Method dataSource</span></span>

<span data-ttu-id="5ae43-145">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-145">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="5ae43-146">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="5ae43-146">Return Value - dataSource</span></span>

<span data-ttu-id="5ae43-147">QueryBuildRange クラスオブジェクトのインスタンスを作成するために使用されたデータソース。</span><span class="sxs-lookup"><span data-stu-id="5ae43-147">The data source that was used to instantiate the QueryBuildRange class object.</span></span>

## <a name="method-doesrangenodebelongtocompositequery"></a><span data-ttu-id="5ae43-148">メソッド doesRangeNodeBelongToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="5ae43-148">Method doesRangeNodeBelongToCompositeQuery</span></span>

```xpp
public boolean doesRangeNodeBelongToCompositeQuery()
```

### <a name="return-value---doesrangenodebelongtocompositequery"></a><span data-ttu-id="5ae43-149">戻り値 - doesRangeNodeBelongToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="5ae43-149">Return Value - doesRangeNodeBelongToCompositeQuery</span></span>

## <a name="method-enabled"></a><span data-ttu-id="5ae43-150">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="5ae43-150">Method enabled</span></span>

<span data-ttu-id="5ae43-151">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-151">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="5ae43-152">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="5ae43-152">Parameters - enabled</span></span>

<span data-ttu-id="5ae43-153">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-153">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="5ae43-154">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="5ae43-154">Return Value - enabled</span></span>

<span data-ttu-id="5ae43-155">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5ae43-155">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="5ae43-156">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="5ae43-156">Remarks - enabled</span></span>

<span data-ttu-id="5ae43-157">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-157">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="5ae43-158">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-158">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="5ae43-159">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-159">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-field"></a><span data-ttu-id="5ae43-160">メソッド field</span><span class="sxs-lookup"><span data-stu-id="5ae43-160">Method field</span></span>

<span data-ttu-id="5ae43-161">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-161">Gets or sets the field ID associated with the object.</span></span>

```xpp
public FieldId field([FieldId value])
```

### <a name="parameters---field"></a><span data-ttu-id="5ae43-162">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="5ae43-162">Parameters - field</span></span>

<span data-ttu-id="5ae43-163">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-163">value</span></span>  

### <a name="return-value---field"></a><span data-ttu-id="5ae43-164">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="5ae43-164">Return Value - field</span></span>

<span data-ttu-id="5ae43-165">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="5ae43-165">The current value of the field ID associated with the object.</span></span>

## <a name="method-fieldarrayindex"></a><span data-ttu-id="5ae43-166">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="5ae43-166">Method fieldArrayIndex</span></span>

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a><span data-ttu-id="5ae43-167">戻り値 - fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="5ae43-167">Return Value - fieldArrayIndex</span></span>

## <a name="method-fieldname"></a><span data-ttu-id="5ae43-168">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="5ae43-168">Method fieldName</span></span>

```xpp
public FieldName fieldName()
```

### <a name="return-value---fieldname"></a><span data-ttu-id="5ae43-169">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="5ae43-169">Return Value - fieldName</span></span>

## <a name="method-label"></a><span data-ttu-id="5ae43-170">メソッド label</span><span class="sxs-lookup"><span data-stu-id="5ae43-170">Method label</span></span>

<span data-ttu-id="5ae43-171">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-171">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="5ae43-172">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="5ae43-172">Parameters - label</span></span>

<span data-ttu-id="5ae43-173">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-173">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="5ae43-174">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="5ae43-174">Return Value - label</span></span>

<span data-ttu-id="5ae43-175">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="5ae43-175">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="5ae43-176">備考 - label</span><span class="sxs-lookup"><span data-stu-id="5ae43-176">Remarks - label</span></span>

<span data-ttu-id="5ae43-177">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-177">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="5ae43-178">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ae43-178">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="5ae43-179">メソッド名</span><span class="sxs-lookup"><span data-stu-id="5ae43-179">Method name</span></span>

<span data-ttu-id="5ae43-180">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-180">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="5ae43-181">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="5ae43-181">Parameters - name</span></span>

<span data-ttu-id="5ae43-182">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-182">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="5ae43-183">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="5ae43-183">Return Value - name</span></span>

<span data-ttu-id="5ae43-184">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="5ae43-184">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="5ae43-185">備考 - name</span><span class="sxs-lookup"><span data-stu-id="5ae43-185">Remarks - name</span></span>

<span data-ttu-id="5ae43-186">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae43-186">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="5ae43-187">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-187">Begins with a letter.</span></span>
-   <span data-ttu-id="5ae43-188">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="5ae43-188">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="5ae43-189">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-189">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="5ae43-190">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ae43-190">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="5ae43-191">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="5ae43-191">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-prompt"></a><span data-ttu-id="5ae43-192">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="5ae43-192">Method prompt</span></span>

```xpp
public str prompt()
```

### <a name="return-value---prompt"></a><span data-ttu-id="5ae43-193">戻り値 - prompt</span><span class="sxs-lookup"><span data-stu-id="5ae43-193">Return Value - prompt</span></span>

## <a name="method-rangetype"></a><span data-ttu-id="5ae43-194">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="5ae43-194">Method rangeType</span></span>

```xpp
public QueryRangeType rangeType([QueryRangeType rangeType])
```

### <a name="parameters---rangetype"></a><span data-ttu-id="5ae43-195">パラメーター - rangeType</span><span class="sxs-lookup"><span data-stu-id="5ae43-195">Parameters - rangeType</span></span>

<span data-ttu-id="5ae43-196">rangeType</span><span class="sxs-lookup"><span data-stu-id="5ae43-196">rangeType</span></span>  

### <a name="return-value---rangetype"></a><span data-ttu-id="5ae43-197">戻り値 - rangeType</span><span class="sxs-lookup"><span data-stu-id="5ae43-197">Return Value - rangeType</span></span>

## <a name="method-status"></a><span data-ttu-id="5ae43-198">メソッド status</span><span class="sxs-lookup"><span data-stu-id="5ae43-198">Method status</span></span>

<span data-ttu-id="5ae43-199">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-199">Gets or sets the status of an object.</span></span>

```xpp
public int status([int value])
```

### <a name="parameters---status"></a><span data-ttu-id="5ae43-200">パラメーター - status</span><span class="sxs-lookup"><span data-stu-id="5ae43-200">Parameters - status</span></span>

<span data-ttu-id="5ae43-201">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-201">value</span></span>  

### <a name="return-value---status"></a><span data-ttu-id="5ae43-202">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="5ae43-202">Return Value - status</span></span>

<span data-ttu-id="5ae43-203">オブジェクトの現在の状態</span><span class="sxs-lookup"><span data-stu-id="5ae43-203">The current status of the object.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="5ae43-204">備考 - status</span><span class="sxs-lookup"><span data-stu-id="5ae43-204">Remarks - status</span></span>

<span data-ttu-id="5ae43-205">ステータスには次の値があります。</span><span class="sxs-lookup"><span data-stu-id="5ae43-205">The following values are possible for the status:</span></span>

-   <span data-ttu-id="5ae43-206">0 � ステータス オープン。</span><span class="sxs-lookup"><span data-stu-id="5ae43-206">0 � Status Open.</span></span>
-   <span data-ttu-id="5ae43-207">1 � ステータス ロック。</span><span class="sxs-lookup"><span data-stu-id="5ae43-207">1 � Status Lock.</span></span>
-   <span data-ttu-id="5ae43-208">2 � ステータスが非表示です。</span><span class="sxs-lookup"><span data-stu-id="5ae43-208">2 � Status Hide.</span></span>

## <a name="method-table"></a><span data-ttu-id="5ae43-209">メソッド table</span><span class="sxs-lookup"><span data-stu-id="5ae43-209">Method table</span></span>

<span data-ttu-id="5ae43-210">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-210">Gets or sets the table ID that is associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="5ae43-211">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="5ae43-211">Parameters - table</span></span>

<span data-ttu-id="5ae43-212">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-212">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="5ae43-213">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="5ae43-213">Return Value - table</span></span>

<span data-ttu-id="5ae43-214">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="5ae43-214">The current value of the table ID that is associated with the object.</span></span>

## <a name="method-tableselector"></a><span data-ttu-id="5ae43-215">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="5ae43-215">Method tableSelector</span></span>

```xpp
public TableId tableSelector([TableId value])
```

### <a name="parameters---tableselector"></a><span data-ttu-id="5ae43-216">パラメーター - tableSelector</span><span class="sxs-lookup"><span data-stu-id="5ae43-216">Parameters - tableSelector</span></span>

<span data-ttu-id="5ae43-217">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-217">value</span></span>  

### <a name="return-value---tableselector"></a><span data-ttu-id="5ae43-218">戻り値 - tableSelector</span><span class="sxs-lookup"><span data-stu-id="5ae43-218">Return Value - tableSelector</span></span>

## <a name="method-tostring"></a><span data-ttu-id="5ae43-219">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="5ae43-219">Method toString</span></span>

<span data-ttu-id="5ae43-220">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-220">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="5ae43-221">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="5ae43-221">Return Value - toString</span></span>

<span data-ttu-id="5ae43-222">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="5ae43-222">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="5ae43-223">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="5ae43-223">Remarks - toString</span></span>

<span data-ttu-id="5ae43-224">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-224">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="5ae43-225">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ae43-225">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="5ae43-226">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-226">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-typeof"></a><span data-ttu-id="5ae43-227">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="5ae43-227">Method typeof</span></span>

```xpp
public int typeof()
```

### <a name="return-value---typeof"></a><span data-ttu-id="5ae43-228">戻り値 - typeof</span><span class="sxs-lookup"><span data-stu-id="5ae43-228">Return Value - typeof</span></span>

## <a name="method-valid"></a><span data-ttu-id="5ae43-229">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="5ae43-229">Method valid</span></span>

```xpp
public boolean valid()
```

### <a name="return-value---valid"></a><span data-ttu-id="5ae43-230">戻り値 - valid</span><span class="sxs-lookup"><span data-stu-id="5ae43-230">Return Value - valid</span></span>

## <a name="method-value"></a><span data-ttu-id="5ae43-231">メソッド value</span><span class="sxs-lookup"><span data-stu-id="5ae43-231">Method value</span></span>

<span data-ttu-id="5ae43-232">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5ae43-232">Gets or sets the value that queried records must match to be retrieved.</span></span>

```xpp
public str value([str value])
```

### <a name="parameters---value"></a><span data-ttu-id="5ae43-233">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="5ae43-233">Parameters - value</span></span>

<span data-ttu-id="5ae43-234">値</span><span class="sxs-lookup"><span data-stu-id="5ae43-234">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="5ae43-235">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="5ae43-235">Return Value - value</span></span>

<span data-ttu-id="5ae43-236">範囲の文字列値</span><span class="sxs-lookup"><span data-stu-id="5ae43-236">The string value for the range.</span></span>

## <a name="method-associaterangenodetocompositequery"></a><span data-ttu-id="5ae43-237">メソッド associateRangeNodeToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="5ae43-237">Method associateRangeNodeToCompositeQuery</span></span>

```xpp
public void associateRangeNodeToCompositeQuery()
```

## <a name="method-finalize"></a><span data-ttu-id="5ae43-238">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="5ae43-238">Method finalize</span></span>

```xpp
public void finalize()
```

