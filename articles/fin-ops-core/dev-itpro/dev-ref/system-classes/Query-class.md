---
title: Query クラス
description: このトピックでは、Query クラスについて説明します。
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
ms.openlocfilehash: a8b5daa9f26ad98fc8e2135c62d2813d99c1cca4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502871"
---
# <a name="class-query"></a><span data-ttu-id="fb2f1-103">クラス クエリ</span><span class="sxs-lookup"><span data-stu-id="fb2f1-103">Class Query</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Query extends TreeNode
```

<span data-ttu-id="fb2f1-104">クエリ クラスには、クエリの構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-104">The Query class embodies the structure of a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2f1-105">備考</span><span class="sxs-lookup"><span data-stu-id="fb2f1-105">Remarks</span></span>

<span data-ttu-id="fb2f1-106">このタイプのオブジェクトは、データベースからレコードをフェッチするために使用されません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-106">Objects of this kind are not used to fetch records from the database.</span></span> <span data-ttu-id="fb2f1-107">代わりに、クエリ オブジェクトを割り当てることができる QueryRun オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-107">Instead, use a QueryRun object that can be assigned a query object.</span></span> <span data-ttu-id="fb2f1-108">クエリの動的な動作は、QueryRun クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-108">The dynamic behavior of a query is defined by the QueryRun class.</span></span> <span data-ttu-id="fb2f1-109">静的なビヘイビアーは、Query クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-109">The static behavior is defined by the Query class.</span></span> <span data-ttu-id="fb2f1-110">クエリには、データベース内のテーブルに対応する 1 つまたは複数のデータ ソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-110">Queries contain one or more data sources that correspond to tables in the database.</span></span> <span data-ttu-id="fb2f1-111">データ ソースを指定するには、QueryBuildDataSource オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-111">The data sources are specified by using QueryBuildDataSource objects.</span></span> <span data-ttu-id="fb2f1-112">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-112">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="fb2f1-113">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-113">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="fb2f1-114">クエリは、ユーザーが、たとえばフォームなどによりフェッチされるレコードを変更する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-114">Queries are used when the user wants to modify the records that are fetched by, for example, a form.</span></span> <span data-ttu-id="fb2f1-115">多くの場合、1 つ以上の範囲は既存のデータ ソースに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-115">One or more ranges are often added to an existing data source.</span></span> <span data-ttu-id="fb2f1-116">範囲を指定するには、queryBuildRange オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-116">Ranges are specified by using queryBuildRange objects.</span></span>

## <a name="examples"></a><span data-ttu-id="fb2f1-117">例</span><span class="sxs-lookup"><span data-stu-id="fb2f1-117">Examples</span></span>

<span data-ttu-id="fb2f1-118">次の例では、QueryRun オブジェクトを作成するために使用されるクエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-118">The following example creates a query object that is used to create a QueryRun object.</span></span>

```xpp
{ 
    Query q = new Query (QueryStr(Cust)); 
    // Use the query to build a queryRun object. 
    QueryRun qr = new QueryRun (q); 
    // Traverse some records. 
    while (qr.next()) 
    { 
        // ... 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="fb2f1-119">メソッド</span><span class="sxs-lookup"><span data-stu-id="fb2f1-119">Methods</span></span>

| <span data-ttu-id="fb2f1-120">方法</span><span class="sxs-lookup"><span data-stu-id="fb2f1-120">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="fb2f1-121">説明</span><span class="sxs-lookup"><span data-stu-id="fb2f1-121">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2f1-122">public Query addBaseQuery(str queryName)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-122">public Query addBaseQuery(str queryName)</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="fb2f1-123">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-123">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span></span>                                            | <span data-ttu-id="fb2f1-124">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-124">Adds a data source to the top level of the query.</span></span>                                                                                         |
| <span data-ttu-id="fb2f1-125">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-125">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span></span>                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-126">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-126">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-127">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-127">public boolean allowCheck(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-128">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-128">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="fb2f1-129">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-129">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-130">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-130">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-131">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-131">public str changedBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="fb2f1-132">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-132">Gets or sets the name of the user who last changed the Query object.</span></span>                                                                      |
| <span data-ttu-id="fb2f1-133">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-133">public Date changedDate(\[Date value\])</span></span>                                                                                                                                | <span data-ttu-id="fb2f1-134">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-134">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="fb2f1-135">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-135">public str changedTime(\[str value\])</span></span>                                                                                                                                  | <span data-ttu-id="fb2f1-136">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-136">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="fb2f1-137">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-137">public int childDataSourceCount()</span></span>                                                                                                                                      | <span data-ttu-id="fb2f1-138">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-138">Counts the number of data sources that are related to the query.</span></span>                                                                          |
| <span data-ttu-id="fb2f1-139">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-139">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                                        | <span data-ttu-id="fb2f1-140">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-140">Returns the child data source that corresponds to the specified number.</span></span>                                                                   |
| <span data-ttu-id="fb2f1-141">public boolean containsAggregateFields()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-141">public boolean containsAggregateFields()</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="fb2f1-142">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-142">public str createdBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="fb2f1-143">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-143">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="fb2f1-144">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-144">public Date creationDate(\[Date value\])</span></span>                                                                                                                               | <span data-ttu-id="fb2f1-145">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-145">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="fb2f1-146">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-146">public str creationTime(\[str value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="fb2f1-147">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-147">public int dataSourceCount()</span></span>                                                                                                                                           | <span data-ttu-id="fb2f1-148">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-148">Returns the total number of data sources for the query, including any embedded data sources.</span></span>                                              |
| <span data-ttu-id="fb2f1-149">public QueryBuildDataSource dataSourceName(str name)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-149">public QueryBuildDataSource dataSourceName(str name)</span></span>                                                                                                                   | <span data-ttu-id="fb2f1-150">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-150">Returns the data source that has the specified name.</span></span>                                                                                      |
| <span data-ttu-id="fb2f1-151">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-151">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span></span>                                                                                                             | <span data-ttu-id="fb2f1-152">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-152">Returns the data source that is specified by the data source number.</span></span>                                                                      |
| <span data-ttu-id="fb2f1-153">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-153">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span></span>                                                                                         | <span data-ttu-id="fb2f1-154">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-154">Returns the data source that the specified table is assigned to.</span></span>                                                                          |
| <span data-ttu-id="fb2f1-155">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-155">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-156">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-156">public str description(\[str value\])</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-157">public boolean equal(Object record)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-157">public boolean equal(Object record)</span></span>                                                                                                                                    | <span data-ttu-id="fb2f1-158">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-158">Evaluates whether one query is equal to another.</span></span>                                                                                          |
| <span data-ttu-id="fb2f1-159">public str exportXML()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-159">public str exportXML()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="fb2f1-160">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-160">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fb2f1-161">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-161">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb2f1-162">public QueryBuildDataSource firstTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-162">public QueryBuildDataSource firstTopLevelDataSource()</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-163">public boolean forceNestedLoop(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-163">public boolean forceNestedLoop(boolean arg)</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="fb2f1-164">public boolean forceSelectOrder(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-164">public boolean forceSelectOrder(boolean arg)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-165">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-165">public str form(\[str value\])</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="fb2f1-166">public container getCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-166">public container getCompanyRange()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="fb2f1-167">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-167">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="fb2f1-168">public int getNextUniqueId()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-168">public int getNextUniqueId()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-169">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-169">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-170">public container getValidTimeStateDateRange()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-170">public container getValidTimeStateDateRange()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-171">public container getValidTimeStateDateTimeRange()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-171">public container getValidTimeStateDateTimeRange()</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-172">public ValidTimeStateQueryType getValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-172">public ValidTimeStateQueryType getValidTimeStateQueryType()</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="fb2f1-173">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-173">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-174">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-174">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-175">public boolean hasMultipleTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-175">public boolean hasMultipleTopLevelDataSource()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="fb2f1-176">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-176">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span></span>                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="fb2f1-177">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-177">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-178">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-178">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-179">public boolean inReport()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-179">public boolean inReport()</span></span>                                                                                                                                              | <span data-ttu-id="fb2f1-180">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-180">Determines whether the query is part of a report.</span></span>                                                                                         |
| <span data-ttu-id="fb2f1-181">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-181">public boolean interactive(\[boolean value\])</span></span>                                                                                                                          | <span data-ttu-id="fb2f1-182">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-182">Specifies whether the query is interactive.</span></span>                                                                                               |
| <span data-ttu-id="fb2f1-183">public boolean isCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-183">public boolean isCompositeQuery()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-184">public boolean isExplicitlyOrdered()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-184">public boolean isExplicitlyOrdered()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="fb2f1-185">public boolean isExplicitlyGrouped()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-185">public boolean isExplicitlyGrouped()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="fb2f1-186">public boolean isPureUnionAll()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-186">public boolean isPureUnionAll()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="fb2f1-187">public boolean isUnionType()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-187">public boolean isUnionType()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-188">public int levelNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-188">public int levelNo(int dataSourceNo)</span></span>                                                                                                                                   | <span data-ttu-id="fb2f1-189">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-189">Determines the level of indentation of the specified data source.</span></span>                                                                         |
| <span data-ttu-id="fb2f1-190">public int levelTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-190">public int levelTable(TableId table, \[int occurrence\])</span></span>                                                                                                               | <span data-ttu-id="fb2f1-191">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-191">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>                  |
| <span data-ttu-id="fb2f1-192">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-192">public int literals(\[int value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="fb2f1-193">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-193">public str name(\[str value\])</span></span>                                                                                                                                         | <span data-ttu-id="fb2f1-194">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-194">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="fb2f1-195">public Query newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-195">public Query newObject(AnyType source)</span></span>                                                                                                                                 | <span data-ttu-id="fb2f1-196">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-196">Creates a query that exists on the same client side or server side as the source query.</span></span>                                                   |
| <span data-ttu-id="fb2f1-197">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-197">public int nextUniqueId(\[int value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="fb2f1-198">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-198">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-199">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-199">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-200">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-200">public Guid origin(\[Guid value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="fb2f1-201">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-201">public container pack(\[boolean doCheck\])</span></span>                                                                                                                             | <span data-ttu-id="fb2f1-202">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-202">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>                              |
| <span data-ttu-id="fb2f1-203">public container packInternals()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-203">public container packInternals()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="fb2f1-204">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-204">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span></span>                                                                                     |                                                                                                                                           |
| <span data-ttu-id="fb2f1-205">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-205">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="fb2f1-206">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-206">public int queryType(\[int value\])</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="fb2f1-207">public str quickFilterValue()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-207">public str quickFilterValue()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-208">public int quickFilterControlId()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-208">public int quickFilterControlId()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-209">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-209">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-210">public Report report()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-210">public Report report()</span></span>                                                                                                                                                 | <span data-ttu-id="fb2f1-211">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-211">Returns the report in which the query is defined, if the report exists.</span></span>                                                                   |
| <span data-ttu-id="fb2f1-212">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-212">public boolean saved()</span></span>                                                                                                                                                 | <span data-ttu-id="fb2f1-213">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-213">Indicates whether the query has been saved to disk.</span></span>                                                                                       |
| <span data-ttu-id="fb2f1-214">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-214">public boolean searchable(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-215">public Guid importSession(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-215">public Guid importSession(\[Guid value\])</span></span>                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="fb2f1-216">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-216">public str title(\[str value\])</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="fb2f1-217">public int topRows(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-217">public int topRows(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-218">public str toString()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-218">public str toString()</span></span>                                                                                                                                                  | <span data-ttu-id="fb2f1-219">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-219">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="fb2f1-220">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-220">public boolean userUpdate(\[boolean value\])</span></span>                                                                                                                           | <span data-ttu-id="fb2f1-221">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-221">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>                                             |
| <span data-ttu-id="fb2f1-222">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-222">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-223">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-223">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span></span>                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-224">public int validTimeStateFlags(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-224">public int validTimeStateFlags(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-225">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-225">public int version(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="fb2f1-226">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-226">public str xml(\[int indent\])</span></span>                                                                                                                                         | <span data-ttu-id="fb2f1-227">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-227">Returns an XML string that represents the current object.</span></span>                                                                                 |
| <span data-ttu-id="fb2f1-228">public void clearBaseQueries()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-228">public void clearBaseQueries()</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="fb2f1-229">public void addCompanyRange(str companyName)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-229">public void addCompanyRange(str companyName)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-230">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-230">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="fb2f1-231">public void clearCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-231">public void clearCompanyRange()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="fb2f1-232">public void unpackInternals(container internalData)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-232">public void unpackInternals(container internalData)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="fb2f1-233">public void new(\[AnyType source\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-233">public void new(\[AnyType source\])</span></span>                                                                                                                                    | <span data-ttu-id="fb2f1-234">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-234">Creates a query object.</span></span>                                                                                                                   |
| <span data-ttu-id="fb2f1-235">public void checkFieldAccess(boolean setCheckFieldAccess)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-235">public void checkFieldAccess(boolean setCheckFieldAccess)</span></span>                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="fb2f1-236">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-236">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="fb2f1-237">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-237">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span></span>                                                                                               |                                                                                                                                           |
| <span data-ttu-id="fb2f1-238">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-238">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="fb2f1-239">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-239">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-240">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-240">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="fb2f1-241">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-241">public void finalize()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="fb2f1-242">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-242">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-243">public void clearOrderBy()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-243">public void clearOrderBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="fb2f1-244">public void clearAllFields()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-244">public void clearAllFields()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="fb2f1-245">public void clearGroupBy()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-245">public void clearGroupBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="fb2f1-246">public void autoAuthzMode(AutoAuthzMode mode)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-246">public void autoAuthzMode(AutoAuthzMode mode)</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-247">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-247">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-248">public void generateCursors()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-248">public void generateCursors()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="fb2f1-249">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span><span class="sxs-lookup"><span data-stu-id="fb2f1-249">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="fb2f1-250">public void addContains(str containsValue, \[boolean prefixSearch\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-250">public void addContains(str containsValue, \[boolean prefixSearch\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="fb2f1-251">public void resetValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="fb2f1-251">public void resetValidTimeStateQueryType()</span></span>                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="fb2f1-252">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-252">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="fb2f1-253">public boolean skipAutoOrderBy(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb2f1-253">public boolean skipAutoOrderBy(\[boolean value\])</span></span>                                                                                                                           | <span data-ttu-id="fb2f1-254">Order By フィールドが明示的に指定されていない場合、Order By 句の自動生成をスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-254">Allows to skip the generation of an automatic Order By clause in case no Order By field was specified explicitly.</span></span>                                             |

## <a name="method-addbasequery"></a><span data-ttu-id="fb2f1-255">メソッド addBaseQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-255">Method addBaseQuery</span></span>

```xpp
public Query addBaseQuery(str queryName)
```

### <a name="parameters---addbasequery"></a><span data-ttu-id="fb2f1-256">パラメーター - addBaseQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-256">Parameters - addBaseQuery</span></span>

<span data-ttu-id="fb2f1-257">queryName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-257">queryName</span></span>  

### <a name="return-value---addbasequery"></a><span data-ttu-id="fb2f1-258">戻り値 - addBaseQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-258">Return Value - addBaseQuery</span></span>

## <a name="method-adddatasource"></a><span data-ttu-id="fb2f1-259">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-259">Method addDataSource</span></span>

<span data-ttu-id="fb2f1-260">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-260">Adds a data source to the top level of the query.</span></span>

```xpp
public QueryBuildDataSource addDataSource(TableId table, [str name], [UnionType unionType], [boolean emptyFieldList])
```

### <a name="parameters---adddatasource"></a><span data-ttu-id="fb2f1-261">パラメーター - addDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-261">Parameters - addDataSource</span></span>

<span data-ttu-id="fb2f1-262">テーブル</span><span class="sxs-lookup"><span data-stu-id="fb2f1-262">table</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-263">名前</span><span class="sxs-lookup"><span data-stu-id="fb2f1-263">name</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-264">unionType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-264">unionType</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-265">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="fb2f1-265">emptyFieldList</span></span>  

### <a name="return-value---adddatasource"></a><span data-ttu-id="fb2f1-266">戻り値 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-266">Return Value - addDataSource</span></span>

<span data-ttu-id="fb2f1-267">作成されたデータ ソース オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-267">The data source object that is created.</span></span>

### <a name="remarks---adddatasource"></a><span data-ttu-id="fb2f1-268">備考 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-268">Remarks - addDataSource</span></span>

<span data-ttu-id="fb2f1-269">文書作成のために名前の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-269">A name value can be specified for documentation purposes.</span></span> <span data-ttu-id="fb2f1-270">dataSourceName メソッドを使用してデータ ソースをフェッチする名前を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-270">You can use the name to fetch the data source by using the dataSourceName method.</span></span>

## <a name="method-addhavingfilter"></a><span data-ttu-id="fb2f1-271">メソッド addHavingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-271">Method addHavingFilter</span></span>

```xpp
public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, [int arrayIndex])
```

### <a name="parameters---addhavingfilter"></a><span data-ttu-id="fb2f1-272">パラメーター - addHavingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-272">Parameters - addHavingFilter</span></span>

<span data-ttu-id="fb2f1-273">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-273">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-274">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-274">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-275">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="fb2f1-275">aggregateFunction</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-276">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-276">arrayIndex</span></span>  

### <a name="return-value---addhavingfilter"></a><span data-ttu-id="fb2f1-277">戻り値 - addHavingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-277">Return Value - addHavingFilter</span></span>

## <a name="method-addqueryfilter"></a><span data-ttu-id="fb2f1-278">メソッド addQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-278">Method addQueryFilter</span></span>

```xpp
public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, [int arrayIndex])
```

### <a name="parameters---addqueryfilter"></a><span data-ttu-id="fb2f1-279">パラメーター - addQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-279">Parameters - addQueryFilter</span></span>

<span data-ttu-id="fb2f1-280">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-280">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-281">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-281">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-282">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-282">arrayIndex</span></span>  

### <a name="return-value---addqueryfilter"></a><span data-ttu-id="fb2f1-283">戻り値 - addQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-283">Return Value - addQueryFilter</span></span>

## <a name="method-allowcheck"></a><span data-ttu-id="fb2f1-284">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="fb2f1-284">Method allowCheck</span></span>

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a><span data-ttu-id="fb2f1-285">パラメーター - allowCheck</span><span class="sxs-lookup"><span data-stu-id="fb2f1-285">Parameters - allowCheck</span></span>

<span data-ttu-id="fb2f1-286">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-286">value</span></span>  

### <a name="return-value---allowcheck"></a><span data-ttu-id="fb2f1-287">戻り値 - allowCheck</span><span class="sxs-lookup"><span data-stu-id="fb2f1-287">Return Value - allowCheck</span></span>

## <a name="method-allowcrosscompany"></a><span data-ttu-id="fb2f1-288">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="fb2f1-288">Method allowCrossCompany</span></span>

```xpp
public boolean allowCrossCompany([boolean value])
```

### <a name="parameters---allowcrosscompany"></a><span data-ttu-id="fb2f1-289">パラメーター - allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="fb2f1-289">Parameters - allowCrossCompany</span></span>

<span data-ttu-id="fb2f1-290">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-290">value</span></span>  

### <a name="return-value---allowcrosscompany"></a><span data-ttu-id="fb2f1-291">戻り値 - allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="fb2f1-291">Return Value - allowCrossCompany</span></span>

## <a name="method-allowhavingfilters"></a><span data-ttu-id="fb2f1-292">メソッド allowHavingFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-292">Method allowHavingFilters</span></span>

```xpp
public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)
```

### <a name="parameters---allowhavingfilters"></a><span data-ttu-id="fb2f1-293">パラメーター - allowHavingFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-293">Parameters - allowHavingFilters</span></span>

<span data-ttu-id="fb2f1-294">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-294">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-295">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-295">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-296">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="fb2f1-296">aggregateFunction</span></span>  

### <a name="return-value---allowhavingfilters"></a><span data-ttu-id="fb2f1-297">戻り値 - allowHavingFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-297">Return Value - allowHavingFilters</span></span>

## <a name="method-allowqueryfilters"></a><span data-ttu-id="fb2f1-298">メソッド allowQueryFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-298">Method allowQueryFilters</span></span>

```xpp
public boolean allowQueryFilters(QueryBuildDataSource dataSource)
```

### <a name="parameters---allowqueryfilters"></a><span data-ttu-id="fb2f1-299">パラメーター - allowQueryFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-299">Parameters - allowQueryFilters</span></span>

<span data-ttu-id="fb2f1-300">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-300">dataSource</span></span>  

### <a name="return-value---allowqueryfilters"></a><span data-ttu-id="fb2f1-301">戻り値 - allowQueryFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-301">Return Value - allowQueryFilters</span></span>

## <a name="method-changedby"></a><span data-ttu-id="fb2f1-302">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-302">Method changedBy</span></span>

<span data-ttu-id="fb2f1-303">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-303">Gets or sets the name of the user who last changed the Query object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="fb2f1-304">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-304">Parameters - changedBy</span></span>

<span data-ttu-id="fb2f1-305">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-305">value</span></span>  
<span data-ttu-id="fb2f1-306">クエリ オブジェクトを最後に変更したユーザーの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-306">The name of the user who last changed the Query object; optional.</span></span>

### <a name="return-value---changedby"></a><span data-ttu-id="fb2f1-307">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-307">Return Value - changedBy</span></span>

<span data-ttu-id="fb2f1-308">クエリ オブジェクトを最後に変更したユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-308">The name of the user who last changed the Query object.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="fb2f1-309">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-309">Method changedDate</span></span>

<span data-ttu-id="fb2f1-310">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-310">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="fb2f1-311">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-311">Parameters - changedDate</span></span>

<span data-ttu-id="fb2f1-312">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-312">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="fb2f1-313">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-313">Return Value - changedDate</span></span>

<span data-ttu-id="fb2f1-314">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-314">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="fb2f1-315">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-315">Method changedTime</span></span>

<span data-ttu-id="fb2f1-316">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-316">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="fb2f1-317">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-317">Parameters - changedTime</span></span>

<span data-ttu-id="fb2f1-318">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-318">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="fb2f1-319">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-319">Return Value - changedTime</span></span>

<span data-ttu-id="fb2f1-320">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-320">The time an application object was last changed.</span></span>

## <a name="method-childdatasourcecount"></a><span data-ttu-id="fb2f1-321">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-321">Method childDataSourceCount</span></span>

<span data-ttu-id="fb2f1-322">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-322">Counts the number of data sources that are related to the query.</span></span>

```xpp
public int childDataSourceCount()
```

### <a name="return-value---childdatasourcecount"></a><span data-ttu-id="fb2f1-323">戻り値 - childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-323">Return Value - childDataSourceCount</span></span>

<span data-ttu-id="fb2f1-324">このクエリに関連するデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-324">The number of data sources that are related to the query.</span></span>

### <a name="remarks---childdatasourcecount"></a><span data-ttu-id="fb2f1-325">備考 - childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-325">Remarks - childDataSourceCount</span></span>

<span data-ttu-id="fb2f1-326">このメソッドは、トップレベルのクエリに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-326">This method is used for the top-level query.</span></span> <span data-ttu-id="fb2f1-327">別のデータ ソースに埋め込まれているデータ ソースの数を確認するには、childDataSourceCount メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-327">To determine the number of data sources that are embedded in another data source, use the childDataSourceCount method.</span></span>

## <a name="method-childdatasourceno"></a><span data-ttu-id="fb2f1-328">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-328">Method childDataSourceNo</span></span>

<span data-ttu-id="fb2f1-329">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-329">Returns the child data source that corresponds to the specified number.</span></span>

```xpp
public QueryBuildDataSource childDataSourceNo(int dataSourceNo)
```

### <a name="parameters---childdatasourceno"></a><span data-ttu-id="fb2f1-330">パラメーター - childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-330">Parameters - childDataSourceNo</span></span>

<span data-ttu-id="fb2f1-331">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-331">dataSourceNo</span></span>  
<span data-ttu-id="fb2f1-332">子データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-332">The number of the child data source.</span></span>

### <a name="return-value---childdatasourceno"></a><span data-ttu-id="fb2f1-333">戻り値 - childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-333">Return Value - childDataSourceNo</span></span>

<span data-ttu-id="fb2f1-334">指定された番号を持つ子データ ソース。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-334">The child data source that has the specified number.</span></span>

### <a name="remarks---childdatasourceno"></a><span data-ttu-id="fb2f1-335">備考 - childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-335">Remarks - childDataSourceNo</span></span>

<span data-ttu-id="fb2f1-336">指定された数値は、クエリのすぐ下にあるデータ ソースを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-336">The number that is specified must represent a data source that is immediately underneath the query.</span></span> <span data-ttu-id="fb2f1-337">通常、このようなデータ ソースは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-337">Typically, there is only one such data source.</span></span>

## <a name="method-containsaggregatefields"></a><span data-ttu-id="fb2f1-338">メソッド containsAggregateFields</span><span class="sxs-lookup"><span data-stu-id="fb2f1-338">Method containsAggregateFields</span></span>

```xpp
public boolean containsAggregateFields()
```

### <a name="return-value---containsaggregatefields"></a><span data-ttu-id="fb2f1-339">戻り値 - containsAggregateFields</span><span class="sxs-lookup"><span data-stu-id="fb2f1-339">Return Value - containsAggregateFields</span></span>

## <a name="method-createdby"></a><span data-ttu-id="fb2f1-340">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-340">Method createdBy</span></span>

<span data-ttu-id="fb2f1-341">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-341">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="fb2f1-342">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-342">Parameters - createdBy</span></span>

<span data-ttu-id="fb2f1-343">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-343">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="fb2f1-344">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-344">Return Value - createdBy</span></span>

<span data-ttu-id="fb2f1-345">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-345">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="fb2f1-346">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-346">Method creationDate</span></span>

<span data-ttu-id="fb2f1-347">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-347">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="fb2f1-348">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-348">Parameters - creationDate</span></span>

<span data-ttu-id="fb2f1-349">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-349">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="fb2f1-350">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-350">Return Value - creationDate</span></span>

<span data-ttu-id="fb2f1-351">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-351">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="fb2f1-352">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-352">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="fb2f1-353">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-353">Parameters - creationTime</span></span>

<span data-ttu-id="fb2f1-354">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-354">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="fb2f1-355">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-355">Return Value - creationTime</span></span>

## <a name="method-datasourcecount"></a><span data-ttu-id="fb2f1-356">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-356">Method dataSourceCount</span></span>

<span data-ttu-id="fb2f1-357">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-357">Returns the total number of data sources for the query, including any embedded data sources.</span></span>

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a><span data-ttu-id="fb2f1-358">戻り値 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-358">Return Value - dataSourceCount</span></span>

<span data-ttu-id="fb2f1-359">このクエリのデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-359">The number of data sources for this query.</span></span>

### <a name="remarks---datasourcecount"></a><span data-ttu-id="fb2f1-360">備考 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-360">Remarks - dataSourceCount</span></span>

<span data-ttu-id="fb2f1-361">この番号は、データ ソースの推移的な番号であり、任意の埋め込みデータ ソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-361">The number is the transitive number of data sources and includes any embedded data sources.</span></span>

## <a name="method-datasourcename"></a><span data-ttu-id="fb2f1-362">メソッド dataSourceName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-362">Method dataSourceName</span></span>

<span data-ttu-id="fb2f1-363">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-363">Returns the data source that has the specified name.</span></span>

```xpp
public QueryBuildDataSource dataSourceName(str name)
```

### <a name="parameters---datasourcename"></a><span data-ttu-id="fb2f1-364">パラメーター - dataSourceName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-364">Parameters - dataSourceName</span></span>

<span data-ttu-id="fb2f1-365">名前</span><span class="sxs-lookup"><span data-stu-id="fb2f1-365">name</span></span>  
<span data-ttu-id="fb2f1-366">返すデータソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-366">The string that contains the name of the data source to return.</span></span>

### <a name="return-value---datasourcename"></a><span data-ttu-id="fb2f1-367">戻り値 - dataSourceName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-367">Return Value - dataSourceName</span></span>

<span data-ttu-id="fb2f1-368">指定した名前を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-368">The data source that has the specified name; an uninitialized object if the specified data source does not exist.</span></span>

## <a name="method-datasourceno"></a><span data-ttu-id="fb2f1-369">メソッド dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-369">Method dataSourceNo</span></span>

<span data-ttu-id="fb2f1-370">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-370">Returns the data source that is specified by the data source number.</span></span>

```xpp
public QueryBuildDataSource dataSourceNo(int dataSourceNo)
```

### <a name="parameters---datasourceno"></a><span data-ttu-id="fb2f1-371">パラメーター - dataSdataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-371">Parameters - dataSourceNo</span></span>

<span data-ttu-id="fb2f1-372">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-372">dataSourceNo</span></span>  
<span data-ttu-id="fb2f1-373">データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-373">The number of the data source.</span></span>

### <a name="return-value---datasourceno"></a><span data-ttu-id="fb2f1-374">戻り値 - dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-374">Return Value - dataSourceNo</span></span>

<span data-ttu-id="fb2f1-375">指定した番号を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-375">The data source that has the specified number; an uninitialized object if the specified data source does not exist.</span></span>

## <a name="method-datasourcetable"></a><span data-ttu-id="fb2f1-376">メソッド dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-376">Method dataSourceTable</span></span>

<span data-ttu-id="fb2f1-377">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-377">Returns the data source that the specified table is assigned to.</span></span>

```xpp
public QueryBuildDataSource dataSourceTable(TableId table, [int occurrence])
```

### <a name="parameters---datasourcetable"></a><span data-ttu-id="fb2f1-378">パラメーター - dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-378">Parameters - dataSourceTable</span></span>

<span data-ttu-id="fb2f1-379">テーブル</span><span class="sxs-lookup"><span data-stu-id="fb2f1-379">table</span></span>  
<span data-ttu-id="fb2f1-380">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-380">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="fb2f1-381">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-381">The default value is 1, which specifies the first (and typically only) instance.</span></span>

<!-- -->

<span data-ttu-id="fb2f1-382">occurrence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-382">occurrence</span></span>  
<span data-ttu-id="fb2f1-383">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-383">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="fb2f1-384">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-384">The default value is 1, which specifies the first (and typically only) instance.</span></span>

### <a name="return-value---datasourcetable"></a><span data-ttu-id="fb2f1-385">戻り値 - dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-385">Return Value - dataSourceTable</span></span>

<span data-ttu-id="fb2f1-386">指定されたテーブルが割り当てられているデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-386">The data source that the specified table is assigned to.</span></span>

### <a name="remarks---datasourcetable"></a><span data-ttu-id="fb2f1-387">備考 - dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-387">Remarks - dataSourceTable</span></span>

<span data-ttu-id="fb2f1-388">データ ソースは、dataSourceNo メソッドまたは dataSourceName メソッドを呼び出すことによって取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-388">The data source can also be retrieved by calling the dataSourceNo method or the dataSourceName method.</span></span>

## <a name="method-datasourceuniqueid"></a><span data-ttu-id="fb2f1-389">メソッド dataSourceUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-389">Method dataSourceUniqueId</span></span>

```xpp
public QueryBuildDataSource dataSourceUniqueId(int uniqueId)
```

### <a name="parameters---datasourceuniqueid"></a><span data-ttu-id="fb2f1-390">パラメーター - dataSourceUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-390">Parameters - dataSourceUniqueId</span></span>

<span data-ttu-id="fb2f1-391">uniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-391">uniqueId</span></span>  

### <a name="return-value---datasourceuniqueid"></a><span data-ttu-id="fb2f1-392">戻り値 - dataSourceUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-392">Return Value - dataSourceUniqueId</span></span>

## <a name="method-description"></a><span data-ttu-id="fb2f1-393">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="fb2f1-393">Method description</span></span>

```xpp
public str description([str value])
```

### <a name="parameters---description"></a><span data-ttu-id="fb2f1-394">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="fb2f1-394">Parameters - description</span></span>

<span data-ttu-id="fb2f1-395">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-395">value</span></span>  

### <a name="return-value---description"></a><span data-ttu-id="fb2f1-396">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="fb2f1-396">Return Value - description</span></span>

## <a name="method-equal"></a><span data-ttu-id="fb2f1-397">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="fb2f1-397">Method equal</span></span>

<span data-ttu-id="fb2f1-398">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-398">Evaluates whether one query is equal to another.</span></span>

```xpp
public boolean equal(Object record)
```

### <a name="parameters---equal"></a><span data-ttu-id="fb2f1-399">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="fb2f1-399">Parameters - equal</span></span>

<span data-ttu-id="fb2f1-400">記録</span><span class="sxs-lookup"><span data-stu-id="fb2f1-400">record</span></span>  
<span data-ttu-id="fb2f1-401">比較として使用するクエリです。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-401">The query to use as a comparison.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="fb2f1-402">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="fb2f1-402">Return Value - equal</span></span>

<span data-ttu-id="fb2f1-403">クエリが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-403">true if the queries are equal; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="fb2f1-404">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="fb2f1-404">Remarks - equal</span></span>

<span data-ttu-id="fb2f1-405">この場合、「等しい」は、クエリが比較されるクエリと構造的に同一であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-405">"Equal" in this case means that the query is structurally identical to the query that it is compared to.</span></span> <span data-ttu-id="fb2f1-406">クエリには、同じファイルに割り当てられたデータ ソースと同じ数のデータ ソースがあり、同じ数の範囲があります。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-406">The query has the same number of data sources assigned to the same files, and it has the same number of ranges.</span></span>

## <a name="method-exportxml"></a><span data-ttu-id="fb2f1-407">メソッド exportXML</span><span class="sxs-lookup"><span data-stu-id="fb2f1-407">Method exportXML</span></span>

```xpp
public str exportXML()
```

### <a name="return-value---exportxml"></a><span data-ttu-id="fb2f1-408">戻り値 - exportXML</span><span class="sxs-lookup"><span data-stu-id="fb2f1-408">Return Value - exportXML</span></span>

## <a name="method-findhavingfilterbyfield"></a><span data-ttu-id="fb2f1-409">メソッド findHavingFilterByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-409">Method findHavingFilterByField</span></span>

```xpp
public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findhavingfilterbyfield"></a><span data-ttu-id="fb2f1-410">パラメーター - findHavingFilterByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-410">Parameters - findHavingFilterByField</span></span>

<span data-ttu-id="fb2f1-411">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-411">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-412">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-412">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-413">occurrence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-413">occurrence</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-414">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-414">arrayIndex</span></span>  

### <a name="return-value---findhavingfilterbyfield"></a><span data-ttu-id="fb2f1-415">戻り値 - findHavingFilterByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-415">Return Value - findHavingFilterByField</span></span>

## <a name="method-findqueryfilter"></a><span data-ttu-id="fb2f1-416">メソッド findQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-416">Method findQueryFilter</span></span>

```xpp
public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findqueryfilter"></a><span data-ttu-id="fb2f1-417">パラメーター - findQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-417">Parameters - findQueryFilter</span></span>

<span data-ttu-id="fb2f1-418">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-418">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-419">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-419">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-420">occurrence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-420">occurrence</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-421">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-421">arrayIndex</span></span>  

### <a name="return-value---findqueryfilter"></a><span data-ttu-id="fb2f1-422">戻り値 - findQueryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-422">Return Value - findQueryFilter</span></span>

## <a name="method-firsttopleveldatasource"></a><span data-ttu-id="fb2f1-423">メソッド firstTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-423">Method firstTopLevelDataSource</span></span>

```xpp
public QueryBuildDataSource firstTopLevelDataSource()
```

### <a name="return-value---firsttopleveldatasource"></a><span data-ttu-id="fb2f1-424">戻り値 - firstTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-424">Return Value - firstTopLevelDataSource</span></span>

## <a name="method-forcenestedloop"></a><span data-ttu-id="fb2f1-425">メソッド forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="fb2f1-425">Method forceNestedLoop</span></span>

```xpp
public boolean forceNestedLoop(boolean arg)
```

### <a name="parameters---forcenestedloop"></a><span data-ttu-id="fb2f1-426">パラメーター - forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="fb2f1-426">Parameters - forceNestedLoop</span></span>

<span data-ttu-id="fb2f1-427">arg</span><span class="sxs-lookup"><span data-stu-id="fb2f1-427">arg</span></span>  

### <a name="return-value---forcenestedloop"></a><span data-ttu-id="fb2f1-428">戻り値 - forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="fb2f1-428">Return Value - forceNestedLoop</span></span>

## <a name="method-forceselectorder"></a><span data-ttu-id="fb2f1-429">メソッド forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="fb2f1-429">Method forceSelectOrder</span></span>

```xpp
public boolean forceSelectOrder(boolean arg)
```

### <a name="parameters---forceselectorder"></a><span data-ttu-id="fb2f1-430">パラメーター - forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="fb2f1-430">Parameters - forceSelectOrder</span></span>

<span data-ttu-id="fb2f1-431">arg</span><span class="sxs-lookup"><span data-stu-id="fb2f1-431">arg</span></span>  

### <a name="return-value---forceselectorder"></a><span data-ttu-id="fb2f1-432">戻り値 - forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="fb2f1-432">Return Value - forceSelectOrder</span></span>

## <a name="method-form"></a><span data-ttu-id="fb2f1-433">メソッド form</span><span class="sxs-lookup"><span data-stu-id="fb2f1-433">Method form</span></span>

```xpp
public str form([str value])
```

### <a name="parameters---form"></a><span data-ttu-id="fb2f1-434">パラメーター - form</span><span class="sxs-lookup"><span data-stu-id="fb2f1-434">Parameters - form</span></span>

<span data-ttu-id="fb2f1-435">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-435">value</span></span>  

### <a name="return-value---form"></a><span data-ttu-id="fb2f1-436">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="fb2f1-436">Return Value - form</span></span>

## <a name="method-getcompanyrange"></a><span data-ttu-id="fb2f1-437">メソッド getCompanyRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-437">Method getCompanyRange</span></span>

```xpp
public container getCompanyRange()
```

### <a name="return-value---getcompanyrange"></a><span data-ttu-id="fb2f1-438">戻り値 - getCompanyRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-438">Return Value - getCompanyRange</span></span>

## <a name="method-getmostrestrictedqueryfilterstatus"></a><span data-ttu-id="fb2f1-439">メソッド getMostRestrictedQueryFilterStatus</span><span class="sxs-lookup"><span data-stu-id="fb2f1-439">Method getMostRestrictedQueryFilterStatus</span></span>

```xpp
public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, [int fieldId])
```

### <a name="parameters---getmostrestrictedqueryfilterstatus"></a><span data-ttu-id="fb2f1-440">パラメーター - getMostRestrictedQueryFilterStatus</span><span class="sxs-lookup"><span data-stu-id="fb2f1-440">Parameters - getMostRestrictedQueryFilterStatus</span></span>

<span data-ttu-id="fb2f1-441">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-441">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-442">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-442">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-443">fieldId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-443">fieldId</span></span>  

### <a name="return-value---getmostrestrictedqueryfilterstatus"></a><span data-ttu-id="fb2f1-444">戻り値 - getMostRestrictedQueryFilterStatus</span><span class="sxs-lookup"><span data-stu-id="fb2f1-444">Return Value - getMostRestrictedQueryFilterStatus</span></span>

## <a name="method-getnextuniqueid"></a><span data-ttu-id="fb2f1-445">メソッド getNextUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-445">Method getNextUniqueId</span></span>

```xpp
public int getNextUniqueId()
```

### <a name="return-value---getnextuniqueid"></a><span data-ttu-id="fb2f1-446">戻り値 - getNextUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-446">Return Value - getNextUniqueId</span></span>

## <a name="method-getsqlstatement"></a><span data-ttu-id="fb2f1-447">メソッド getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="fb2f1-447">Method getSQLStatement</span></span>

```xpp
public str getSQLStatement([boolean noRuntimeOptimization])
```

### <a name="parameters---getsqlstatement"></a><span data-ttu-id="fb2f1-448">パラメーター - getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="fb2f1-448">Parameters - getSQLStatement</span></span>

<span data-ttu-id="fb2f1-449">noRuntimeOptimization</span><span class="sxs-lookup"><span data-stu-id="fb2f1-449">noRuntimeOptimization</span></span>  

### <a name="return-value---getsqlstatement"></a><span data-ttu-id="fb2f1-450">戻り値 - getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="fb2f1-450">Return Value - getSQLStatement</span></span>

## <a name="method-getvalidtimestatedaterange"></a><span data-ttu-id="fb2f1-451">メソッド getValidTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-451">Method getValidTimeStateDateRange</span></span>

```xpp
public container getValidTimeStateDateRange()
```

### <a name="return-value---getvalidtimestatedaterange"></a><span data-ttu-id="fb2f1-452">戻り値 - getValidTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-452">Return Value - getValidTimeStateDateRange</span></span>

## <a name="method-getvalidtimestatedatetimerange"></a><span data-ttu-id="fb2f1-453">メソッド getValidTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-453">Method getValidTimeStateDateTimeRange</span></span>

```xpp
public container getValidTimeStateDateTimeRange()
```

### <a name="return-value---getvalidtimestatedatetimerange"></a><span data-ttu-id="fb2f1-454">戻り値 - getValidTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-454">Return Value - getValidTimeStateDateTimeRange</span></span>

## <a name="method-getvalidtimestatequerytype"></a><span data-ttu-id="fb2f1-455">メソッド getValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-455">Method getValidTimeStateQueryType</span></span>

```xpp
public ValidTimeStateQueryType getValidTimeStateQueryType()
```

### <a name="return-value---getvalidtimestatequerytype"></a><span data-ttu-id="fb2f1-456">戻り値 - getValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-456">Return Value - getValidTimeStateQueryType</span></span>

## <a name="method-groupbyfield"></a><span data-ttu-id="fb2f1-457">メソッド groupByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-457">Method groupByField</span></span>

```xpp
public QueryGroupByField groupByField(int index, [QueryBuildDataSource dataSource])
```

### <a name="parameters---groupbyfield"></a><span data-ttu-id="fb2f1-458">パラメーター - groupByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-458">Parameters - groupByField</span></span>

<span data-ttu-id="fb2f1-459">指数</span><span class="sxs-lookup"><span data-stu-id="fb2f1-459">index</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-460">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-460">dataSource</span></span>  

### <a name="return-value---groupbyfield"></a><span data-ttu-id="fb2f1-461">戻り値 - groupByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-461">Return Value - groupByField</span></span>

## <a name="method-groupbyfieldcount"></a><span data-ttu-id="fb2f1-462">メソッド groupByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-462">Method groupByFieldCount</span></span>

```xpp
public int groupByFieldCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---groupbyfieldcount"></a><span data-ttu-id="fb2f1-463">パラメーター - groupByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-463">Parameters - groupByFieldCount</span></span>

<span data-ttu-id="fb2f1-464">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-464">dataSource</span></span>  

### <a name="return-value---groupbyfieldcount"></a><span data-ttu-id="fb2f1-465">戻り値 - groupByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-465">Return Value - groupByFieldCount</span></span>

## <a name="method-hasmultipletopleveldatasource"></a><span data-ttu-id="fb2f1-466">メソッド hasMultipleTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-466">Method hasMultipleTopLevelDataSource</span></span>

```xpp
public boolean hasMultipleTopLevelDataSource()
```

### <a name="return-value---hasmultipletopleveldatasource"></a><span data-ttu-id="fb2f1-467">戻り値 - hasMultipleTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-467">Return Value - hasMultipleTopLevelDataSource</span></span>

## <a name="method-hasrangeorfilter"></a><span data-ttu-id="fb2f1-468">メソッド hasRangeOrFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-468">Method hasRangeOrFilter</span></span>

```xpp
public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)
```

### <a name="parameters---hasrangeorfilter"></a><span data-ttu-id="fb2f1-469">パラメーター - hasRangeOrFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-469">Parameters - hasRangeOrFilter</span></span>

<span data-ttu-id="fb2f1-470">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-470">dataSource</span></span>  

### <a name="return-value---hasrangeorfilter"></a><span data-ttu-id="fb2f1-471">戻り値 - hasRangeOrFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-471">Return Value - hasRangeOrFilter</span></span>

## <a name="method-havingfilter"></a><span data-ttu-id="fb2f1-472">メソッド havingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-472">Method havingFilter</span></span>

```xpp
public QueryHavingFilter havingFilter(int count, [QueryBuildDataSource dataSource])
```

### <a name="parameters---havingfilter"></a><span data-ttu-id="fb2f1-473">パラメーター - havingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-473">Parameters - havingFilter</span></span>

<span data-ttu-id="fb2f1-474">カウント</span><span class="sxs-lookup"><span data-stu-id="fb2f1-474">count</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-475">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-475">dataSource</span></span>  

### <a name="return-value---havingfilter"></a><span data-ttu-id="fb2f1-476">戻り値 - havingFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-476">Return Value - havingFilter</span></span>

## <a name="method-havingfiltercount"></a><span data-ttu-id="fb2f1-477">メソッド havingFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-477">Method havingFilterCount</span></span>

```xpp
public int havingFilterCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---havingfiltercount"></a><span data-ttu-id="fb2f1-478">パラメーター - havingFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-478">Parameters - havingFilterCount</span></span>

<span data-ttu-id="fb2f1-479">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-479">dataSource</span></span>  

### <a name="return-value---havingfiltercount"></a><span data-ttu-id="fb2f1-480">戻り値 - havingFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-480">Return Value - havingFilterCount</span></span>

## <a name="method-inreport"></a><span data-ttu-id="fb2f1-481">メソッド inReport</span><span class="sxs-lookup"><span data-stu-id="fb2f1-481">Method inReport</span></span>

<span data-ttu-id="fb2f1-482">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-482">Determines whether the query is part of a report.</span></span>

```xpp
public boolean inReport()
```

### <a name="return-value---inreport"></a><span data-ttu-id="fb2f1-483">戻り値 - inReport</span><span class="sxs-lookup"><span data-stu-id="fb2f1-483">Return Value - inReport</span></span>

<span data-ttu-id="fb2f1-484">クエリがレポートの一部である場合は (レポートのデータ ソース ノードの下にある場合は) true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-484">true if the query is part of a report (is found under a report's data sources node); otherwise, false.</span></span>

### <a name="remarks---inreport"></a><span data-ttu-id="fb2f1-485">備考 - inReport</span><span class="sxs-lookup"><span data-stu-id="fb2f1-485">Remarks - inReport</span></span>

<span data-ttu-id="fb2f1-486">この関数は、通常アプリケーション コードでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-486">This function is not typically used by application code.</span></span> <span data-ttu-id="fb2f1-487">メソッドが true を返す場合は、レポート メソッドはクエリが定義されているレポートにアクセスするために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-487">If the method returns true, the report method can be used to access the report in which the query is defined.</span></span>

## <a name="method-interactive"></a><span data-ttu-id="fb2f1-488">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="fb2f1-488">Method interactive</span></span>

<span data-ttu-id="fb2f1-489">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-489">Specifies whether the query is interactive.</span></span>

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a><span data-ttu-id="fb2f1-490">パラメーター - interactive</span><span class="sxs-lookup"><span data-stu-id="fb2f1-490">Parameters - interactive</span></span>

<span data-ttu-id="fb2f1-491">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-491">value</span></span>  
<span data-ttu-id="fb2f1-492">クエリがインタラクティブかどうかを示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-492">A value that indicates whether the query is interactive; optional.</span></span>

### <a name="return-value---interactive"></a><span data-ttu-id="fb2f1-493">戻り値 - interactive</span><span class="sxs-lookup"><span data-stu-id="fb2f1-493">Return Value - interactive</span></span>

<span data-ttu-id="fb2f1-494">クエリが対話形式である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-494">true if the query is interactive; otherwise, false.</span></span>

### <a name="remarks---interactive"></a><span data-ttu-id="fb2f1-495">備考 - interactive</span><span class="sxs-lookup"><span data-stu-id="fb2f1-495">Remarks - interactive</span></span>

<span data-ttu-id="fb2f1-496">対話型クエリでは、たとえば prompt メソッドが呼び出されたときに、クエリはユーザーにダイアログ ボックスを提示できます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-496">In an interactive query, the query can, for example, present the user with a dialog box when the prompt method is called.</span></span> <span data-ttu-id="fb2f1-497">この機能は、コードをバッチに送信する場合や、コードを無人で実行する必要がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-497">This functionality is used when code will be submitted to a batch and in other situations where code must run unattended.</span></span>

## <a name="method-iscompositequery"></a><span data-ttu-id="fb2f1-498">メソッド isCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-498">Method isCompositeQuery</span></span>

```xpp
public boolean isCompositeQuery()
```

### <a name="return-value---iscompositequery"></a><span data-ttu-id="fb2f1-499">備考 - isCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-499">Return Value - isCompositeQuery</span></span>

## <a name="method-isexplicitlyordered"></a><span data-ttu-id="fb2f1-500">メソッド isExplicitlyOrdered</span><span class="sxs-lookup"><span data-stu-id="fb2f1-500">Method isExplicitlyOrdered</span></span>

```xpp
public boolean isExplicitlyOrdered()
```

### <a name="return-value---isexplicitlyordered"></a><span data-ttu-id="fb2f1-501">戻り値 - isExplicitlyOrdered</span><span class="sxs-lookup"><span data-stu-id="fb2f1-501">Return Value - isExplicitlyOrdered</span></span>

## <a name="method-isexplicitlygrouped"></a><span data-ttu-id="fb2f1-502">メソッド isExplicitlyGrouped</span><span class="sxs-lookup"><span data-stu-id="fb2f1-502">Method isExplicitlyGrouped</span></span>

```xpp
public boolean isExplicitlyGrouped()
```

### <a name="return-value---isexplicitlygrouped"></a><span data-ttu-id="fb2f1-503">戻り値 - isExplicitlyGrouped</span><span class="sxs-lookup"><span data-stu-id="fb2f1-503">Return Value - isExplicitlyGrouped</span></span>

## <a name="method-ispureunionall"></a><span data-ttu-id="fb2f1-504">メソッド isPureUnionAll</span><span class="sxs-lookup"><span data-stu-id="fb2f1-504">Method isPureUnionAll</span></span>

```xpp
public boolean isPureUnionAll()
```

### <a name="return-value---ispureunionall"></a><span data-ttu-id="fb2f1-505">戻り値 - isPureUnionAll</span><span class="sxs-lookup"><span data-stu-id="fb2f1-505">Return Value - isPureUnionAll</span></span>

## <a name="method-isuniontype"></a><span data-ttu-id="fb2f1-506">メソッド isUnionType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-506">Method isUnionType</span></span>

```xpp
public boolean isUnionType()
```

### <a name="return-value---isuniontype"></a><span data-ttu-id="fb2f1-507">戻り値 - isUnionType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-507">Return Value - isUnionType</span></span>

## <a name="method-levelno"></a><span data-ttu-id="fb2f1-508">メソッド levelNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-508">Method levelNo</span></span>

<span data-ttu-id="fb2f1-509">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-509">Determines the level of indentation of the specified data source.</span></span>

```xpp
public int levelNo(int dataSourceNo)
```

### <a name="parameters---levelno"></a><span data-ttu-id="fb2f1-510">パラメーター - levelNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-510">Parameters - levelNo</span></span>

<span data-ttu-id="fb2f1-511">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-511">dataSourceNo</span></span>  
<span data-ttu-id="fb2f1-512">データ ソースのレベルを決定する番号。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-512">The data source number to determine the level for.</span></span>

### <a name="return-value---levelno"></a><span data-ttu-id="fb2f1-513">戻り値 - levelNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-513">Return Value - levelNo</span></span>

<span data-ttu-id="fb2f1-514">指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-514">The level number of the specified data source.</span></span>

### <a name="remarks---levelno"></a><span data-ttu-id="fb2f1-515">備考 - levelNo</span><span class="sxs-lookup"><span data-stu-id="fb2f1-515">Remarks - levelNo</span></span>

<span data-ttu-id="fb2f1-516">データソースは、1 から順に番号付けされます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-516">The data sources are numbered consecutively, starting at 1.</span></span>

## <a name="method-leveltable"></a><span data-ttu-id="fb2f1-517">メソッド levelTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-517">Method levelTable</span></span>

<span data-ttu-id="fb2f1-518">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-518">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>

```xpp
public int levelTable(TableId table, [int occurrence])
```

### <a name="parameters---leveltable"></a><span data-ttu-id="fb2f1-519">パラメーター - levelTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-519">Parameters - levelTable</span></span>

<span data-ttu-id="fb2f1-520">テーブル</span><span class="sxs-lookup"><span data-stu-id="fb2f1-520">table</span></span>  
<span data-ttu-id="fb2f1-521">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-521">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

<!-- -->

<span data-ttu-id="fb2f1-522">occurrence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-522">occurrence</span></span>  
<span data-ttu-id="fb2f1-523">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-523">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

### <a name="return-value---leveltable"></a><span data-ttu-id="fb2f1-524">戻り値 - levelTable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-524">Return Value - levelTable</span></span>

<span data-ttu-id="fb2f1-525">クエリの指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-525">The level number of the query's specified data source.</span></span>

## <a name="method-literals"></a><span data-ttu-id="fb2f1-526">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-526">Method literals</span></span>

```xpp
public int literals([int value])
```

### <a name="parameters---literals"></a><span data-ttu-id="fb2f1-527">パラメーター - literals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-527">Parameters - literals</span></span>

<span data-ttu-id="fb2f1-528">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-528">value</span></span>  

### <a name="return-value---literals"></a><span data-ttu-id="fb2f1-529">戻り値 - literals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-529">Return Value - literals</span></span>

## <a name="method-name"></a><span data-ttu-id="fb2f1-530">メソッド名</span><span class="sxs-lookup"><span data-stu-id="fb2f1-530">Method name</span></span>

<span data-ttu-id="fb2f1-531">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-531">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="fb2f1-532">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="fb2f1-532">Parameters - name</span></span>

<span data-ttu-id="fb2f1-533">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-533">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="fb2f1-534">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="fb2f1-534">Return Value - name</span></span>

<span data-ttu-id="fb2f1-535">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-535">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="fb2f1-536">備考 - name</span><span class="sxs-lookup"><span data-stu-id="fb2f1-536">Remarks - name</span></span>

<span data-ttu-id="fb2f1-537">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-537">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="fb2f1-538">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-538">Begins with a letter.</span></span>
-   <span data-ttu-id="fb2f1-539">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-539">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="fb2f1-540">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-540">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="fb2f1-541">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-541">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="fb2f1-542">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-542">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-newobject"></a><span data-ttu-id="fb2f1-543">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="fb2f1-543">Method newObject</span></span>

<span data-ttu-id="fb2f1-544">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-544">Creates a query that exists on the same client side or server side as the source query.</span></span>

```xpp
public Query newObject(AnyType source)
```

### <a name="parameters---newobject"></a><span data-ttu-id="fb2f1-545">パラメーター - newObject</span><span class="sxs-lookup"><span data-stu-id="fb2f1-545">Parameters - newObject</span></span>

<span data-ttu-id="fb2f1-546">ソース</span><span class="sxs-lookup"><span data-stu-id="fb2f1-546">source</span></span>  
<span data-ttu-id="fb2f1-547">ソース クエリ。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-547">The source query.</span></span>

### <a name="return-value---newobject"></a><span data-ttu-id="fb2f1-548">戻り値 - newObject</span><span class="sxs-lookup"><span data-stu-id="fb2f1-548">Return Value - newObject</span></span>

<span data-ttu-id="fb2f1-549">新しいクエリ。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-549">The new query.</span></span>

## <a name="method-nextuniqueid"></a><span data-ttu-id="fb2f1-550">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-550">Method nextUniqueId</span></span>

```xpp
public int nextUniqueId([int value])
```

### <a name="parameters---nextuniqueid"></a><span data-ttu-id="fb2f1-551">パラメーター - nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-551">Parameters - nextUniqueId</span></span>

<span data-ttu-id="fb2f1-552">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-552">value</span></span>  

### <a name="return-value---nextuniqueid"></a><span data-ttu-id="fb2f1-553">戻り値 - nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-553">Return Value - nextUniqueId</span></span>

## <a name="method-orderbyfield"></a><span data-ttu-id="fb2f1-554">メソッド orderByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-554">Method orderByField</span></span>

```xpp
public QueryOrderByField orderByField(int index, [QueryBuildDataSource dataSource])
```

### <a name="parameters---orderbyfield"></a><span data-ttu-id="fb2f1-555">パラメーター - orderByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-555">Parameters - orderByField</span></span>

<span data-ttu-id="fb2f1-556">指数</span><span class="sxs-lookup"><span data-stu-id="fb2f1-556">index</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-557">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-557">dataSource</span></span>  

### <a name="return-value---orderbyfield"></a><span data-ttu-id="fb2f1-558">戻り値 - orderByField</span><span class="sxs-lookup"><span data-stu-id="fb2f1-558">Return Value - orderByField</span></span>

## <a name="method-orderbyfieldcount"></a><span data-ttu-id="fb2f1-559">メソッド orderByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-559">Method orderByFieldCount</span></span>

```xpp
public int orderByFieldCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---orderbyfieldcount"></a><span data-ttu-id="fb2f1-560">パラメーター - orderByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-560">Parameters - orderByFieldCount</span></span>

<span data-ttu-id="fb2f1-561">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-561">dataSource</span></span>  

### <a name="return-value---orderbyfieldcount"></a><span data-ttu-id="fb2f1-562">戻り値 - orderByFieldCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-562">Return Value - orderByFieldCount</span></span>

## <a name="method-origin"></a><span data-ttu-id="fb2f1-563">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="fb2f1-563">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="fb2f1-564">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="fb2f1-564">Parameters - origin</span></span>

<span data-ttu-id="fb2f1-565">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-565">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="fb2f1-566">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="fb2f1-566">Return Value - origin</span></span>

## <a name="method-pack"></a><span data-ttu-id="fb2f1-567">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="fb2f1-567">Method pack</span></span>

<span data-ttu-id="fb2f1-568">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-568">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>

```xpp
public container pack([boolean doCheck])
```

### <a name="parameters---pack"></a><span data-ttu-id="fb2f1-569">パラメーター - pack</span><span class="sxs-lookup"><span data-stu-id="fb2f1-569">Parameters - pack</span></span>

<span data-ttu-id="fb2f1-570">doCheck</span><span class="sxs-lookup"><span data-stu-id="fb2f1-570">doCheck</span></span>  
<span data-ttu-id="fb2f1-571">クエリのデーターソースが外部のカーソルを参照する (クエリのデータソースを外部のカーソルへリンクするなど) ときに、エラーフラグを設定するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-571">A Boolean value that indicates whether to flag an error when a data source in the query references an outside cursor, such as a link to a cursor that is foreign to the query's data source; optional.</span></span> <span data-ttu-id="fb2f1-572">既定値は、true で、制約が適用されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-572">The default value is true, which enforces the constraint.</span></span>

### <a name="return-value---pack"></a><span data-ttu-id="fb2f1-573">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="fb2f1-573">Return Value - pack</span></span>

<span data-ttu-id="fb2f1-574">クエリを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-574">The container that holds the query.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="fb2f1-575">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="fb2f1-575">Remarks - pack</span></span>

<span data-ttu-id="fb2f1-576">このメソッドで作成されたコンテナーは、新しいメソッドまたは newObject メソッドのいずれかを使用して query オブジェクトまたは queryRun オブジェクトをインスタンス化するときに入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-576">The container that is created by this method can serve as input when you instantiate a query or queryRun object by using either the new method or the newObject method.</span></span> <span data-ttu-id="fb2f1-577">クエリのデータ ソースとは異なるカーソルへのリンクは、コンテナーにパックされません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-577">Links to cursors that are foreign to the query's data source are not packed into the container.</span></span> <span data-ttu-id="fb2f1-578">この種類のリンクをパックする必要がある場合は、カーソルのデータのスナップショットを取得し、各フィールドの範囲を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-578">If you must pack this kind of link, you should take a snapshot of the cursor's data and construct ranges for each field.</span></span>

## <a name="method-packinternals"></a><span data-ttu-id="fb2f1-579">メソッド packInternals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-579">Method packInternals</span></span>

```xpp
public container packInternals()
```

### <a name="return-value---packinternals"></a><span data-ttu-id="fb2f1-580">戻り値 - packInternals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-580">Return Value - packInternals</span></span>

## <a name="method-queryfilter"></a><span data-ttu-id="fb2f1-581">メソッド queryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-581">Method queryFilter</span></span>

```xpp
public QueryFilter queryFilter(int count, [QueryBuildDataSource rootDataSource])
```

### <a name="parameters---queryfilter"></a><span data-ttu-id="fb2f1-582">パラメーター - queryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-582">Parameters - queryFilter</span></span>

<span data-ttu-id="fb2f1-583">カウント</span><span class="sxs-lookup"><span data-stu-id="fb2f1-583">count</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-584">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-584">rootDataSource</span></span>  

### <a name="return-value---queryfilter"></a><span data-ttu-id="fb2f1-585">戻り値 - queryFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-585">Return Value - queryFilter</span></span>

## <a name="method-queryfiltercount"></a><span data-ttu-id="fb2f1-586">メソッド queryFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-586">Method queryFilterCount</span></span>

```xpp
public int queryFilterCount([QueryBuildDataSource rootDataSource])
```

### <a name="parameters---queryfiltercount"></a><span data-ttu-id="fb2f1-587">パラメーター - queryFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-587">Parameters - queryFilterCount</span></span>

<span data-ttu-id="fb2f1-588">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-588">rootDataSource</span></span>  

### <a name="return-value---queryfiltercount"></a><span data-ttu-id="fb2f1-589">戻り値 - queryFilterCount</span><span class="sxs-lookup"><span data-stu-id="fb2f1-589">Return Value - queryFilterCount</span></span>

## <a name="method-querytype"></a><span data-ttu-id="fb2f1-590">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-590">Method queryType</span></span>

```xpp
public int queryType([int value])
```

### <a name="parameters---querytype"></a><span data-ttu-id="fb2f1-591">パラメーター - queryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-591">Parameters - queryType</span></span>

<span data-ttu-id="fb2f1-592">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-592">value</span></span>  

### <a name="return-value---querytype"></a><span data-ttu-id="fb2f1-593">戻り値 - queryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-593">Return Value - queryType</span></span>

## <a name="method-quickfiltervalue"></a><span data-ttu-id="fb2f1-594">メソッド quickFilterValue</span><span class="sxs-lookup"><span data-stu-id="fb2f1-594">Method quickFilterValue</span></span>

```xpp
public str quickFilterValue()
```

### <a name="return-value---quickfiltervalue"></a><span data-ttu-id="fb2f1-595">戻り値 - quickFilterValue</span><span class="sxs-lookup"><span data-stu-id="fb2f1-595">Return Value - quickFilterValue</span></span>

## <a name="method-quickfiltercontrolid"></a><span data-ttu-id="fb2f1-596">メソッド quickFilterControlId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-596">Method quickFilterControlId</span></span>

```xpp
public int quickFilterControlId()
```

### <a name="return-value---quickfiltercontrolid"></a><span data-ttu-id="fb2f1-597">戻り値 - quickFilterControlId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-597">Return Value - quickFilterControlId</span></span>

## <a name="method-recordlevelsecurity"></a><span data-ttu-id="fb2f1-598">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fb2f1-598">Method recordLevelSecurity</span></span>

```xpp
public boolean recordLevelSecurity([boolean value])
```

### <a name="parameters---recordlevelsecurity"></a><span data-ttu-id="fb2f1-599">パラメーター - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fb2f1-599">Parameters - recordLevelSecurity</span></span>

<span data-ttu-id="fb2f1-600">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-600">value</span></span>  

### <a name="return-value---recordlevelsecurity"></a><span data-ttu-id="fb2f1-601">戻り値 - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fb2f1-601">Return Value - recordLevelSecurity</span></span>

## <a name="method-report"></a><span data-ttu-id="fb2f1-602">メソッド report</span><span class="sxs-lookup"><span data-stu-id="fb2f1-602">Method report</span></span>

<span data-ttu-id="fb2f1-603">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-603">Returns the report in which the query is defined, if the report exists.</span></span>

```xpp
public Report report()
```

### <a name="return-value---report"></a><span data-ttu-id="fb2f1-604">戻り値 - report</span><span class="sxs-lookup"><span data-stu-id="fb2f1-604">Return Value - report</span></span>

<span data-ttu-id="fb2f1-605">クエリがデータ ソース ノードの下で定義されているレポート。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-605">The report in which the query is defined under the data sources node.</span></span>

### <a name="remarks---report"></a><span data-ttu-id="fb2f1-606">備考 - report</span><span class="sxs-lookup"><span data-stu-id="fb2f1-606">Remarks - report</span></span>

<span data-ttu-id="fb2f1-607">クエリは、必ずしもレポートのコンテキストで定義されているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-607">A query is not necessarily defined in the context of a report.</span></span> <span data-ttu-id="fb2f1-608">レポートのコンテキストでクエリが定義されているかどうかを確認するには、inReport メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-608">To determine whether a query is defined in the context of a report, you can use the inReport method.</span></span>

## <a name="method-saved"></a><span data-ttu-id="fb2f1-609">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="fb2f1-609">Method saved</span></span>

<span data-ttu-id="fb2f1-610">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-610">Indicates whether the query has been saved to disk.</span></span>

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a><span data-ttu-id="fb2f1-611">戻り値 - saved</span><span class="sxs-lookup"><span data-stu-id="fb2f1-611">Return Value - saved</span></span>

<span data-ttu-id="fb2f1-612">クエリがディスクに保存されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-612">true if the query has been saved to disk; otherwise, false.</span></span>

## <a name="method-searchable"></a><span data-ttu-id="fb2f1-613">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-613">Method searchable</span></span>

```xpp
public boolean searchable([boolean value])
```

### <a name="parameters---searchable"></a><span data-ttu-id="fb2f1-614">パラメーター - searchable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-614">Parameters - searchable</span></span>

<span data-ttu-id="fb2f1-615">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-615">value</span></span>  

### <a name="return-value---searchable"></a><span data-ttu-id="fb2f1-616">戻り値 - searchable</span><span class="sxs-lookup"><span data-stu-id="fb2f1-616">Return Value - searchable</span></span>

## <a name="method-importsession"></a><span data-ttu-id="fb2f1-617">メソッド importSession</span><span class="sxs-lookup"><span data-stu-id="fb2f1-617">Method importSession</span></span>

```xpp
public Guid importSession([Guid value])
```

### <a name="parameters---importsession"></a><span data-ttu-id="fb2f1-618">パラメーター - importSession</span><span class="sxs-lookup"><span data-stu-id="fb2f1-618">Parameters - importSession</span></span>

<span data-ttu-id="fb2f1-619">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-619">value</span></span>  

### <a name="return-value---importsession"></a><span data-ttu-id="fb2f1-620">戻り値 - importSession</span><span class="sxs-lookup"><span data-stu-id="fb2f1-620">Return Value - importSession</span></span>

## <a name="method-title"></a><span data-ttu-id="fb2f1-621">メソッド title</span><span class="sxs-lookup"><span data-stu-id="fb2f1-621">Method title</span></span>

```xpp
public str title([str value])
```

### <a name="parameters---title"></a><span data-ttu-id="fb2f1-622">パラメーター - title</span><span class="sxs-lookup"><span data-stu-id="fb2f1-622">Parameters - title</span></span>

<span data-ttu-id="fb2f1-623">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-623">value</span></span>  

### <a name="return-value---title"></a><span data-ttu-id="fb2f1-624">戻り値 - title</span><span class="sxs-lookup"><span data-stu-id="fb2f1-624">Return Value - title</span></span>

## <a name="method-toprows"></a><span data-ttu-id="fb2f1-625">メソッド topRows</span><span class="sxs-lookup"><span data-stu-id="fb2f1-625">Method topRows</span></span>

```xpp
public int topRows([int value])
```

### <a name="parameters---toprows"></a><span data-ttu-id="fb2f1-626">パラメーター - topRows</span><span class="sxs-lookup"><span data-stu-id="fb2f1-626">Parameters - topRows</span></span>

<span data-ttu-id="fb2f1-627">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-627">value</span></span>  

### <a name="return-value---toprows"></a><span data-ttu-id="fb2f1-628">戻り値 - topRows</span><span class="sxs-lookup"><span data-stu-id="fb2f1-628">Return Value - topRows</span></span>

## <a name="method-tostring"></a><span data-ttu-id="fb2f1-629">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="fb2f1-629">Method toString</span></span>

<span data-ttu-id="fb2f1-630">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-630">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="fb2f1-631">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="fb2f1-631">Return Value - toString</span></span>

<span data-ttu-id="fb2f1-632">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-632">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="fb2f1-633">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="fb2f1-633">Remarks - toString</span></span>

<span data-ttu-id="fb2f1-634">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-634">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="fb2f1-635">ただし、メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-635">However, the method can be overridden in a derived class so that it returns values that are meaningful for that type.</span></span> <span data-ttu-id="fb2f1-636">たとえば、SysMethodInfo クラスのインスタンスは、メソッド名、およびインスタンスまたは静的などのメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-636">For example, an instance of the SysMethodInfo class returns the method name, and the type of method, such as Instance or Static.</span></span>

## <a name="method-userupdate"></a><span data-ttu-id="fb2f1-637">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-637">Method userUpdate</span></span>

<span data-ttu-id="fb2f1-638">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-638">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>

```xpp
public boolean userUpdate([boolean value])
```

### <a name="parameters---userupdate"></a><span data-ttu-id="fb2f1-639">パラメーター - userUpdate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-639">Parameters - userUpdate</span></span>

<span data-ttu-id="fb2f1-640">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-640">value</span></span>  
<span data-ttu-id="fb2f1-641">フェッチされたレコードをクエリが更新できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-641">A Boolean value that indicates whether the query can update the records that it fetches; optional.</span></span>

### <a name="return-value---userupdate"></a><span data-ttu-id="fb2f1-642">戻り値 - userUpdate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-642">Return Value - userUpdate</span></span>

<span data-ttu-id="fb2f1-643">クエリがフェッチ対象のレコードを現在更新することができる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-643">true if the query can currently update records that it fetches; otherwise false.</span></span>

## <a name="method-validtimestateasofdate"></a><span data-ttu-id="fb2f1-644">メソッド validTimeStateAsOfDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-644">Method validTimeStateAsOfDate</span></span>

```xpp
public Date validTimeStateAsOfDate([Date asOfDate])
```

### <a name="parameters---validtimestateasofdate"></a><span data-ttu-id="fb2f1-645">パラメーター - validTimeStateAsOfDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-645">Parameters - validTimeStateAsOfDate</span></span>

<span data-ttu-id="fb2f1-646">asOfDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-646">asOfDate</span></span>  

### <a name="return-value---validtimestateasofdate"></a><span data-ttu-id="fb2f1-647">戻り値 - validTimeStateAsOfDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-647">Return Value - validTimeStateAsOfDate</span></span>

## <a name="method-validtimestateasofdatetime"></a><span data-ttu-id="fb2f1-648">メソッド validTimeStateAsOfDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-648">Method validTimeStateAsOfDateTime</span></span>

```xpp
public DateTime validTimeStateAsOfDateTime([DateTime asOfDateTime])
```

### <a name="parameters---validtimestateasofdatetime"></a><span data-ttu-id="fb2f1-649">パラメーター - validTimeStateAsOfDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-649">Parameters - validTimeStateAsOfDateTime</span></span>

<span data-ttu-id="fb2f1-650">asOfDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-650">asOfDateTime</span></span>  

### <a name="return-value---validtimestateasofdatetime"></a><span data-ttu-id="fb2f1-651">戻り値 - validTimeStateAsOfDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-651">Return Value - validTimeStateAsOfDateTime</span></span>

## <a name="method-validtimestateflags"></a><span data-ttu-id="fb2f1-652">メソッド validTimeStateFlags</span><span class="sxs-lookup"><span data-stu-id="fb2f1-652">Method validTimeStateFlags</span></span>

```xpp
public int validTimeStateFlags([int value])
```

### <a name="parameters---validtimestateflags"></a><span data-ttu-id="fb2f1-653">パラメーター - validTimeStateFlags</span><span class="sxs-lookup"><span data-stu-id="fb2f1-653">Parameters - validTimeStateFlags</span></span>

<span data-ttu-id="fb2f1-654">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-654">value</span></span>  

### <a name="return-value---validtimestateflags"></a><span data-ttu-id="fb2f1-655">戻り値 - validTimeStateFlags</span><span class="sxs-lookup"><span data-stu-id="fb2f1-655">Return Value - validTimeStateFlags</span></span>

## <a name="method-version"></a><span data-ttu-id="fb2f1-656">メソッド version</span><span class="sxs-lookup"><span data-stu-id="fb2f1-656">Method version</span></span>

```xpp
public int version([int value])
```

### <a name="parameters---version"></a><span data-ttu-id="fb2f1-657">パラメーター - version</span><span class="sxs-lookup"><span data-stu-id="fb2f1-657">Parameters - version</span></span>

<span data-ttu-id="fb2f1-658">値</span><span class="sxs-lookup"><span data-stu-id="fb2f1-658">value</span></span>  

### <a name="return-value---version"></a><span data-ttu-id="fb2f1-659">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="fb2f1-659">Return Value - version</span></span>

## <a name="method-xml"></a><span data-ttu-id="fb2f1-660">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="fb2f1-660">Method xml</span></span>

<span data-ttu-id="fb2f1-661">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-661">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="fb2f1-662">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="fb2f1-662">Parameters - xml</span></span>

<span data-ttu-id="fb2f1-663">インデント</span><span class="sxs-lookup"><span data-stu-id="fb2f1-663">indent</span></span>  
<span data-ttu-id="fb2f1-664">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-664">The amount of indentation for the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="fb2f1-665">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="fb2f1-665">Return Value - xml</span></span>

<span data-ttu-id="fb2f1-666">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-666">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="fb2f1-667">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="fb2f1-667">Remarks - xml</span></span>

<span data-ttu-id="fb2f1-668">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-668">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-clearbasequeries"></a><span data-ttu-id="fb2f1-669">メソッド clearBaseQueries</span><span class="sxs-lookup"><span data-stu-id="fb2f1-669">Method clearBaseQueries</span></span>

```xpp
public void clearBaseQueries()
```

## <a name="method-addcompanyrange"></a><span data-ttu-id="fb2f1-670">メソッド addCompanyRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-670">Method addCompanyRange</span></span>

```xpp
public void addCompanyRange(str companyName)
```

### <a name="parameters---addcompanyrange"></a><span data-ttu-id="fb2f1-671">パラメーター - addCompanyRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-671">Parameters - addCompanyRange</span></span>

<span data-ttu-id="fb2f1-672">companyName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-672">companyName</span></span>  

## <a name="method-checkrangeparsingerrors"></a><span data-ttu-id="fb2f1-673">メソッド checkRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-673">Method checkRangeParsingErrors</span></span>

```xpp
public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)
```

### <a name="parameters---checkrangeparsingerrors"></a><span data-ttu-id="fb2f1-674">パラメーター - checkRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-674">Parameters - checkRangeParsingErrors</span></span>

<span data-ttu-id="fb2f1-675">setCheckRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-675">setCheckRangeParsingErrors</span></span>  

## <a name="method-clearcompanyrange"></a><span data-ttu-id="fb2f1-676">メソッド clearCompanyRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-676">Method clearCompanyRange</span></span>

```xpp
public void clearCompanyRange()
```

## <a name="method-unpackinternals"></a><span data-ttu-id="fb2f1-677">メソッド unpackInternals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-677">Method unpackInternals</span></span>

```xpp
public void unpackInternals(container internalData)
```

### <a name="parameters---unpackinternals"></a><span data-ttu-id="fb2f1-678">パラメーター - unpackInternals</span><span class="sxs-lookup"><span data-stu-id="fb2f1-678">Parameters - unpackInternals</span></span>

<span data-ttu-id="fb2f1-679">internalData</span><span class="sxs-lookup"><span data-stu-id="fb2f1-679">internalData</span></span>  

## <a name="method-new"></a><span data-ttu-id="fb2f1-680">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fb2f1-680">Method new</span></span>

<span data-ttu-id="fb2f1-681">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-681">Creates a query object.</span></span>

```xpp
public void new([AnyType source])
```

### <a name="parameters---new"></a><span data-ttu-id="fb2f1-682">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="fb2f1-682">Parameters - new</span></span>

<span data-ttu-id="fb2f1-683">ソース</span><span class="sxs-lookup"><span data-stu-id="fb2f1-683">source</span></span>  
<span data-ttu-id="fb2f1-684">クエリ オブジェクトを基にするソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-684">The source to base the query object on; optional.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="fb2f1-685">備考 - new</span><span class="sxs-lookup"><span data-stu-id="fb2f1-685">Remarks - new</span></span>

<span data-ttu-id="fb2f1-686">このメソッドが呼び出されときに引数が指定されていない場合、将来使用するために、アプリケーション オブジェクト ツリー (AOT) で保存されていない一時的なクエリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb2f1-686">If no arguments are supplied when this method is called, a temporary query is created that is not stored in the Application Object Tree (AOT) for subsequent use.</span></span>

## <a name="method-checkfieldaccess"></a><span data-ttu-id="fb2f1-687">メソッド checkFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fb2f1-687">Method checkFieldAccess</span></span>

```xpp
public void checkFieldAccess(boolean setCheckFieldAccess)
```

### <a name="parameters---checkfieldaccess"></a><span data-ttu-id="fb2f1-688">パラメーター - checkFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fb2f1-688">Parameters - checkFieldAccess</span></span>

<span data-ttu-id="fb2f1-689">setCheckFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fb2f1-689">setCheckFieldAccess</span></span>  

## <a name="method-usedbcacheongeneratedcursors"></a><span data-ttu-id="fb2f1-690">メソッド useDbCacheOnGeneratedCursors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-690">Method useDbCacheOnGeneratedCursors</span></span>

```xpp
public void useDbCacheOnGeneratedCursors([int fetchsize])
```

### <a name="parameters---usedbcacheongeneratedcursors"></a><span data-ttu-id="fb2f1-691">パラメーター - useDbCacheOnGeneratedCursors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-691">Parameters - useDbCacheOnGeneratedCursors</span></span>

<span data-ttu-id="fb2f1-692">fetchsize</span><span class="sxs-lookup"><span data-stu-id="fb2f1-692">fetchsize</span></span>  

## <a name="method-setvalidtimestatequerytype"></a><span data-ttu-id="fb2f1-693">メソッド setValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-693">Method setValidTimeStateQueryType</span></span>

```xpp
public void setValidTimeStateQueryType([ValidTimeStateQueryType type])
```

### <a name="parameters---setvalidtimestatequerytype"></a><span data-ttu-id="fb2f1-694">パラメーター - setValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-694">Parameters - setValidTimeStateQueryType</span></span>

<span data-ttu-id="fb2f1-695">タイプ</span><span class="sxs-lookup"><span data-stu-id="fb2f1-695">type</span></span>  

## <a name="method-validtimestatedaterange"></a><span data-ttu-id="fb2f1-696">メソッド validTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-696">Method validTimeStateDateRange</span></span>

```xpp
public void validTimeStateDateRange([Date fromDate], [Date toDate])
```

### <a name="parameters---validtimestatedaterange"></a><span data-ttu-id="fb2f1-697">パラメーター - validTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-697">Parameters - validTimeStateDateRange</span></span>

<span data-ttu-id="fb2f1-698">fromDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-698">fromDate</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-699">toDate</span><span class="sxs-lookup"><span data-stu-id="fb2f1-699">toDate</span></span>  

## <a name="method-clearhavingfilters"></a><span data-ttu-id="fb2f1-700">メソッド clearHavingFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-700">Method clearHavingFilters</span></span>

```xpp
public void clearHavingFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])
```

### <a name="parameters---clearhavingfilters"></a><span data-ttu-id="fb2f1-701">パラメーター - clearHavingFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-701">Parameters - clearHavingFilters</span></span>

<span data-ttu-id="fb2f1-702">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-702">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-703">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-703">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-704">occurence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-704">occurence</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-705">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-705">arrayIndex</span></span>  

## <a name="method-quickfilter"></a><span data-ttu-id="fb2f1-706">メソッド quickFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-706">Method quickFilter</span></span>

```xpp
public void quickFilter([str dataSourceName], [int tableId], [int fieldId], [str filterValue], [int controlId], [boolean useEqualityComparisonForStrings])
```

### <a name="parameters---quickfilter"></a><span data-ttu-id="fb2f1-707">パラメーター - quickFilter</span><span class="sxs-lookup"><span data-stu-id="fb2f1-707">Parameters - quickFilter</span></span>

<span data-ttu-id="fb2f1-708">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-708">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-709">tableId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-709">tableId</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-710">fieldId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-710">fieldId</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-711">filterValue</span><span class="sxs-lookup"><span data-stu-id="fb2f1-711">filterValue</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-712">controlId</span><span class="sxs-lookup"><span data-stu-id="fb2f1-712">controlId</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-713">useEqualityComparisonForStrings</span><span class="sxs-lookup"><span data-stu-id="fb2f1-713">useEqualityComparisonForStrings</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="fb2f1-714">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="fb2f1-714">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-clearqueryfilters"></a><span data-ttu-id="fb2f1-715">メソッド clearQueryFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-715">Method clearQueryFilters</span></span>

```xpp
public void clearQueryFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])
```

### <a name="parameters---clearqueryfilters"></a><span data-ttu-id="fb2f1-716">パラメーター - clearQueryFilters</span><span class="sxs-lookup"><span data-stu-id="fb2f1-716">Parameters - clearQueryFilters</span></span>

<span data-ttu-id="fb2f1-717">dataSource</span><span class="sxs-lookup"><span data-stu-id="fb2f1-717">dataSource</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-718">fieldName</span><span class="sxs-lookup"><span data-stu-id="fb2f1-718">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-719">occurence</span><span class="sxs-lookup"><span data-stu-id="fb2f1-719">occurence</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-720">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb2f1-720">arrayIndex</span></span>  

## <a name="method-clearorderby"></a><span data-ttu-id="fb2f1-721">メソッド clearOrderBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-721">Method clearOrderBy</span></span>

```xpp
public void clearOrderBy()
```

## <a name="method-clearallfields"></a><span data-ttu-id="fb2f1-722">メソッド clearAllFields</span><span class="sxs-lookup"><span data-stu-id="fb2f1-722">Method clearAllFields</span></span>

```xpp
public void clearAllFields()
```

## <a name="method-cleargroupby"></a><span data-ttu-id="fb2f1-723">メソッド clearGroupBy</span><span class="sxs-lookup"><span data-stu-id="fb2f1-723">Method clearGroupBy</span></span>

```xpp
public void clearGroupBy()
```

## <a name="method-autoauthzmode"></a><span data-ttu-id="fb2f1-724">メソッド autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="fb2f1-724">Method autoAuthzMode</span></span>

```xpp
public void autoAuthzMode(AutoAuthzMode mode)
```

### <a name="parameters---autoauthzmode"></a><span data-ttu-id="fb2f1-725">パラメーター - autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="fb2f1-725">Parameters - autoAuthzMode</span></span>

<span data-ttu-id="fb2f1-726">モード</span><span class="sxs-lookup"><span data-stu-id="fb2f1-726">mode</span></span>  

## <a name="method-insert_recordset"></a><span data-ttu-id="fb2f1-727">メソッド insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="fb2f1-727">Method insert\_recordset</span></span>

```xpp
public static void insert_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)
```

### <a name="parameters---insert_recordset"></a><span data-ttu-id="fb2f1-728">パラメーター - insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="fb2f1-728">Parameters - insert\_recordset</span></span>

<span data-ttu-id="fb2f1-729">targetCursor</span><span class="sxs-lookup"><span data-stu-id="fb2f1-729">targetCursor</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-730">targetToSourceMap</span><span class="sxs-lookup"><span data-stu-id="fb2f1-730">targetToSourceMap</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-731">sourceQuery</span><span class="sxs-lookup"><span data-stu-id="fb2f1-731">sourceQuery</span></span>  

## <a name="method-generatecursors"></a><span data-ttu-id="fb2f1-732">メソッド generateCursors</span><span class="sxs-lookup"><span data-stu-id="fb2f1-732">Method generateCursors</span></span>

```xpp
public void generateCursors()
```

## <a name="method-checkauthorizationonopenranges"></a><span data-ttu-id="fb2f1-733">メソッド checkAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="fb2f1-733">Method checkAuthorizationOnOpenRanges</span></span>

```xpp
public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)
```

### <a name="parameters---checkauthorizationonopenranges"></a><span data-ttu-id="fb2f1-734">パラメーター - checkAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="fb2f1-734">Parameters - checkAuthorizationOnOpenRanges</span></span>

<span data-ttu-id="fb2f1-735">setCheckAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="fb2f1-735">setCheckAuthorizationOnOpenRanges</span></span>  

## <a name="method-addcontains"></a><span data-ttu-id="fb2f1-736">メソッド addContains</span><span class="sxs-lookup"><span data-stu-id="fb2f1-736">Method addContains</span></span>

```xpp
public void addContains(str containsValue, [boolean prefixSearch])
```

### <a name="parameters---addcontains"></a><span data-ttu-id="fb2f1-737">パラメーター -addContains</span><span class="sxs-lookup"><span data-stu-id="fb2f1-737">Parameters - addContains</span></span>

<span data-ttu-id="fb2f1-738">containsValue</span><span class="sxs-lookup"><span data-stu-id="fb2f1-738">containsValue</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-739">prefixSearch</span><span class="sxs-lookup"><span data-stu-id="fb2f1-739">prefixSearch</span></span>  

## <a name="method-resetvalidtimestatequerytype"></a><span data-ttu-id="fb2f1-740">メソッド resetValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="fb2f1-740">Method resetValidTimeStateQueryType</span></span>

```xpp
public void resetValidTimeStateQueryType()
```

## <a name="method-validtimestatedatetimerange"></a><span data-ttu-id="fb2f1-741">メソッド validTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-741">Method validTimeStateDateTimeRange</span></span>

```xpp
public void validTimeStateDateTimeRange([DateTime fromDateTime], [DateTime toDateTime])
```

### <a name="parameters---validtimestatedatetimerange"></a><span data-ttu-id="fb2f1-742">パラメーター - validTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="fb2f1-742">Parameters - validTimeStateDateTimeRange</span></span>

<span data-ttu-id="fb2f1-743">fromDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-743">fromDateTime</span></span>  

<!-- -->

<span data-ttu-id="fb2f1-744">toDateTime</span><span class="sxs-lookup"><span data-stu-id="fb2f1-744">toDateTime</span></span>  

