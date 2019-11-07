---
title: Q クラス
description: 文字 Q で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 51831
ms.assetid: 279efb4c-e228-4ab5-be7d-c96d91064787
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1eb2e4552dfc1f06f17c1aa54a2b04675917f1e2
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627575"
---
# <a name="q-classes"></a><span data-ttu-id="edd9b-103">Q クラス</span><span class="sxs-lookup"><span data-stu-id="edd9b-103">Q classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edd9b-104">文字 Q で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="edd9b-104">System API classes that start with the letter Q.</span></span>

<a name="class-query"></a><span data-ttu-id="edd9b-105">クラス クエリ</span><span class="sxs-lookup"><span data-stu-id="edd9b-105">Class Query</span></span>
-----------

    class Query extends TreeNode

<span data-ttu-id="edd9b-106">クエリ クラスには、クエリの構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-106">The Query class embodies the structure of a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-107">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-107">Remarks</span></span>

<span data-ttu-id="edd9b-108">このタイプのオブジェクトは、データベースからレコードをフェッチするために使用されません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-108">Objects of this kind are not used to fetch records from the database.</span></span> <span data-ttu-id="edd9b-109">代わりに、クエリ オブジェクトを割り当てることができる QueryRun オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-109">Instead, use a QueryRun object that can be assigned a query object.</span></span> <span data-ttu-id="edd9b-110">クエリの動的な動作は、QueryRun クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-110">The dynamic behavior of a query is defined by the QueryRun class.</span></span> <span data-ttu-id="edd9b-111">静的なビヘイビアーは、Query クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-111">The static behavior is defined by the Query class.</span></span> <span data-ttu-id="edd9b-112">クエリには、データベース内のテーブルに対応する 1 つまたは複数のデータ ソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-112">Queries contain one or more data sources that correspond to tables in the database.</span></span> <span data-ttu-id="edd9b-113">データ ソースを指定するには、QueryBuildDataSource オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-113">The data sources are specified by using QueryBuildDataSource objects.</span></span> <span data-ttu-id="edd9b-114">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-114">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="edd9b-115">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-115">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="edd9b-116">クエリは、ユーザーが、たとえばフォームなどによりフェッチされるレコードを変更する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-116">Queries are used when the user wants to modify the records that are fetched by, for example, a form.</span></span> <span data-ttu-id="edd9b-117">多くの場合、1 つ以上の範囲は既存のデータ ソースに追加されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-117">One or more ranges are often added to an existing data source.</span></span> <span data-ttu-id="edd9b-118">範囲を指定するには、queryBuildRange オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-118">Ranges are specified by using queryBuildRange objects.</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-119">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-119">Examples</span></span>

<span data-ttu-id="edd9b-120">次の例では、QueryRun オブジェクトを作成するために使用されるクエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-120">The following example creates a query object that is used to create a QueryRun object.</span></span>

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

### <a name="methods"></a><span data-ttu-id="edd9b-121">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-121">Methods</span></span>

| <span data-ttu-id="edd9b-122">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-122">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="edd9b-123">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-123">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-124">public Query addBaseQuery(str queryName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-124">public Query addBaseQuery(str queryName)</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-125">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-125">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span></span>                                            | <span data-ttu-id="edd9b-126">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-126">Adds a data source to the top level of the query.</span></span>                                                                                         |
| <span data-ttu-id="edd9b-127">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-127">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span></span>                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-128">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-128">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-129">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-129">public boolean allowCheck(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-130">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-130">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-131">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span><span class="sxs-lookup"><span data-stu-id="edd9b-131">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-132">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="edd9b-132">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-133">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-133">public str changedBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="edd9b-134">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-134">Gets or sets the name of the user who last changed the Query object.</span></span>                                                                      |
| <span data-ttu-id="edd9b-135">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-135">public Date changedDate(\[Date value\])</span></span>                                                                                                                                | <span data-ttu-id="edd9b-136">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-136">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="edd9b-137">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-137">public str changedTime(\[str value\])</span></span>                                                                                                                                  | <span data-ttu-id="edd9b-138">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-138">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="edd9b-139">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-139">public int childDataSourceCount()</span></span>                                                                                                                                      | <span data-ttu-id="edd9b-140">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-140">Counts the number of data sources that are related to the query.</span></span>                                                                          |
| <span data-ttu-id="edd9b-141">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-141">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                                        | <span data-ttu-id="edd9b-142">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-142">Returns the child data source that corresponds to the specified number.</span></span>                                                                   |
| <span data-ttu-id="edd9b-143">public boolean containsAggregateFields()</span><span class="sxs-lookup"><span data-stu-id="edd9b-143">public boolean containsAggregateFields()</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-144">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-144">public str createdBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="edd9b-145">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-145">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="edd9b-146">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-146">public Date creationDate(\[Date value\])</span></span>                                                                                                                               | <span data-ttu-id="edd9b-147">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-147">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="edd9b-148">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-148">public str creationTime(\[str value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-149">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-149">public int dataSourceCount()</span></span>                                                                                                                                           | <span data-ttu-id="edd9b-150">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-150">Returns the total number of data sources for the query, including any embedded data sources.</span></span>                                              |
| <span data-ttu-id="edd9b-151">public QueryBuildDataSource dataSourceName(str name)</span><span class="sxs-lookup"><span data-stu-id="edd9b-151">public QueryBuildDataSource dataSourceName(str name)</span></span>                                                                                                                   | <span data-ttu-id="edd9b-152">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-152">Returns the data source that has the specified name.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-153">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-153">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span></span>                                                                                                             | <span data-ttu-id="edd9b-154">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-154">Returns the data source that is specified by the data source number.</span></span>                                                                      |
| <span data-ttu-id="edd9b-155">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-155">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span></span>                                                                                         | <span data-ttu-id="edd9b-156">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-156">Returns the data source that the specified table is assigned to.</span></span>                                                                          |
| <span data-ttu-id="edd9b-157">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span><span class="sxs-lookup"><span data-stu-id="edd9b-157">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-158">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-158">public str description(\[str value\])</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-159">public boolean equal(Object record)</span><span class="sxs-lookup"><span data-stu-id="edd9b-159">public boolean equal(Object record)</span></span>                                                                                                                                    | <span data-ttu-id="edd9b-160">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-160">Evaluates whether one query is equal to another.</span></span>                                                                                          |
| <span data-ttu-id="edd9b-161">public str exportXML()</span><span class="sxs-lookup"><span data-stu-id="edd9b-161">public str exportXML()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-162">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-162">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-163">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-163">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-164">public QueryBuildDataSource firstTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-164">public QueryBuildDataSource firstTopLevelDataSource()</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-165">public boolean forceNestedLoop(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="edd9b-165">public boolean forceNestedLoop(boolean arg)</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-166">public boolean forceSelectOrder(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="edd9b-166">public boolean forceSelectOrder(boolean arg)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-167">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-167">public str form(\[str value\])</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-168">public container getCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="edd9b-168">public container getCompanyRange()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-169">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-169">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-170">public int getNextUniqueId()</span><span class="sxs-lookup"><span data-stu-id="edd9b-170">public int getNextUniqueId()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-171">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-171">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-172">public container getValidTimeStateDateRange()</span><span class="sxs-lookup"><span data-stu-id="edd9b-172">public container getValidTimeStateDateRange()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-173">public container getValidTimeStateDateTimeRange()</span><span class="sxs-lookup"><span data-stu-id="edd9b-173">public container getValidTimeStateDateTimeRange()</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-174">public ValidTimeStateQueryType getValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="edd9b-174">public ValidTimeStateQueryType getValidTimeStateQueryType()</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-175">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-175">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-176">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-176">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-177">public boolean hasMultipleTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-177">public boolean hasMultipleTopLevelDataSource()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-178">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="edd9b-178">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span></span>                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-179">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-179">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-180">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-180">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-181">public boolean inReport()</span><span class="sxs-lookup"><span data-stu-id="edd9b-181">public boolean inReport()</span></span>                                                                                                                                              | <span data-ttu-id="edd9b-182">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-182">Determines whether the query is part of a report.</span></span>                                                                                         |
| <span data-ttu-id="edd9b-183">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-183">public boolean interactive(\[boolean value\])</span></span>                                                                                                                          | <span data-ttu-id="edd9b-184">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-184">Specifies whether the query is interactive.</span></span>                                                                                               |
| <span data-ttu-id="edd9b-185">public boolean isCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="edd9b-185">public boolean isCompositeQuery()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-186">public boolean isExplicitlyOrdered()</span><span class="sxs-lookup"><span data-stu-id="edd9b-186">public boolean isExplicitlyOrdered()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-187">public boolean isExplicitlyGrouped()</span><span class="sxs-lookup"><span data-stu-id="edd9b-187">public boolean isExplicitlyGrouped()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-188">public boolean isPureUnionAll()</span><span class="sxs-lookup"><span data-stu-id="edd9b-188">public boolean isPureUnionAll()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-189">public boolean isUnionType()</span><span class="sxs-lookup"><span data-stu-id="edd9b-189">public boolean isUnionType()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-190">public int levelNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-190">public int levelNo(int dataSourceNo)</span></span>                                                                                                                                   | <span data-ttu-id="edd9b-191">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-191">Determines the level of indentation of the specified data source.</span></span>                                                                         |
| <span data-ttu-id="edd9b-192">public int levelTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-192">public int levelTable(TableId table, \[int occurrence\])</span></span>                                                                                                               | <span data-ttu-id="edd9b-193">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-193">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>                  |
| <span data-ttu-id="edd9b-194">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-194">public int literals(\[int value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-195">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-195">public str name(\[str value\])</span></span>                                                                                                                                         | <span data-ttu-id="edd9b-196">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-196">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="edd9b-197">public Query newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="edd9b-197">public Query newObject(AnyType source)</span></span>                                                                                                                                 | <span data-ttu-id="edd9b-198">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-198">Creates a query that exists on the same client side or server side as the source query.</span></span>                                                   |
| <span data-ttu-id="edd9b-199">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-199">public int nextUniqueId(\[int value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-200">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-200">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-201">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-201">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-202">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-202">public Guid origin(\[Guid value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-203">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-203">public container pack(\[boolean doCheck\])</span></span>                                                                                                                             | <span data-ttu-id="edd9b-204">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-204">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>                              |
| <span data-ttu-id="edd9b-205">public container packInternals()</span><span class="sxs-lookup"><span data-stu-id="edd9b-205">public container packInternals()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-206">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-206">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span></span>                                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-207">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-207">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-208">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-208">public int queryType(\[int value\])</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-209">public str quickFilterValue()</span><span class="sxs-lookup"><span data-stu-id="edd9b-209">public str quickFilterValue()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-210">public int quickFilterControlId()</span><span class="sxs-lookup"><span data-stu-id="edd9b-210">public int quickFilterControlId()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-211">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-211">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-212">public Report report()</span><span class="sxs-lookup"><span data-stu-id="edd9b-212">public Report report()</span></span>                                                                                                                                                 | <span data-ttu-id="edd9b-213">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-213">Returns the report in which the query is defined, if the report exists.</span></span>                                                                   |
| <span data-ttu-id="edd9b-214">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="edd9b-214">public boolean saved()</span></span>                                                                                                                                                 | <span data-ttu-id="edd9b-215">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-215">Indicates whether the query has been saved to disk.</span></span>                                                                                       |
| <span data-ttu-id="edd9b-216">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-216">public boolean searchable(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-217">public Guid importSession(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-217">public Guid importSession(\[Guid value\])</span></span>                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-218">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-218">public str title(\[str value\])</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-219">public int topRows(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-219">public int topRows(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-220">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-220">public str toString()</span></span>                                                                                                                                                  | <span data-ttu-id="edd9b-221">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-221">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-222">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-222">public boolean userUpdate(\[boolean value\])</span></span>                                                                                                                           | <span data-ttu-id="edd9b-223">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-223">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>                                             |
| <span data-ttu-id="edd9b-224">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-224">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-225">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-225">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span></span>                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-226">public int validTimeStateFlags(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-226">public int validTimeStateFlags(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-227">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-227">public int version(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-228">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-228">public str xml(\[int indent\])</span></span>                                                                                                                                         | <span data-ttu-id="edd9b-229">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-229">Returns an XML string that represents the current object.</span></span>                                                                                 |
| <span data-ttu-id="edd9b-230">public void clearBaseQueries()</span><span class="sxs-lookup"><span data-stu-id="edd9b-230">public void clearBaseQueries()</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-231">public void addCompanyRange(str companyName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-231">public void addCompanyRange(str companyName)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-232">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span><span class="sxs-lookup"><span data-stu-id="edd9b-232">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-233">public void clearCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="edd9b-233">public void clearCompanyRange()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-234">public void unpackInternals(container internalData)</span><span class="sxs-lookup"><span data-stu-id="edd9b-234">public void unpackInternals(container internalData)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-235">public void new(\[AnyType source\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-235">public void new(\[AnyType source\])</span></span>                                                                                                                                    | <span data-ttu-id="edd9b-236">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-236">Creates a query object.</span></span>                                                                                                                   |
| <span data-ttu-id="edd9b-237">public void checkFieldAccess(boolean setCheckFieldAccess)</span><span class="sxs-lookup"><span data-stu-id="edd9b-237">public void checkFieldAccess(boolean setCheckFieldAccess)</span></span>                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-238">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-238">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-239">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-239">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span></span>                                                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-240">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-240">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-241">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-241">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-242">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-242">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-243">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-243">public void finalize()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-244">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-244">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-245">public void clearOrderBy()</span><span class="sxs-lookup"><span data-stu-id="edd9b-245">public void clearOrderBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-246">public void clearAllFields()</span><span class="sxs-lookup"><span data-stu-id="edd9b-246">public void clearAllFields()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-247">public void clearGroupBy()</span><span class="sxs-lookup"><span data-stu-id="edd9b-247">public void clearGroupBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-248">public void autoAuthzMode(AutoAuthzMode mode)</span><span class="sxs-lookup"><span data-stu-id="edd9b-248">public void autoAuthzMode(AutoAuthzMode mode)</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-249">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span><span class="sxs-lookup"><span data-stu-id="edd9b-249">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-250">public void generateCursors()</span><span class="sxs-lookup"><span data-stu-id="edd9b-250">public void generateCursors()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-251">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span><span class="sxs-lookup"><span data-stu-id="edd9b-251">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-252">public void addContains(str containsValue, \[boolean prefixSearch\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-252">public void addContains(str containsValue, \[boolean prefixSearch\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-253">public void resetValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="edd9b-253">public void resetValidTimeStateQueryType()</span></span>                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-254">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-254">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-255">public boolean skipAutoOrderBy(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-255">public boolean skipAutoOrderBy(\[boolean value\])</span></span>                                                                                                                           | <span data-ttu-id="edd9b-256">Order By フィールドが明示的に指定されていない場合、Order By 句の自動生成をスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-256">Allows to skip the generation of an automatic Order By clause in case no Order By field was specified explicitly.</span></span>                                             |

### <a name="method-addbasequery"></a><span data-ttu-id="edd9b-257">メソッド addBaseQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-257">Method addBaseQuery</span></span>

    public Query addBaseQuery(str queryName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-258">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-258">Parameters</span></span>

<span data-ttu-id="edd9b-259">queryName</span><span class="sxs-lookup"><span data-stu-id="edd9b-259">queryName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-260">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-260">Return Value</span></span>

### <a name="method-adddatasource"></a><span data-ttu-id="edd9b-261">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-261">Method addDataSource</span></span>

<span data-ttu-id="edd9b-262">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-262">Adds a data source to the top level of the query.</span></span>

    public QueryBuildDataSource addDataSource(TableId table, [str name], [UnionType unionType], [boolean emptyFieldList])

#### <a name="parameters"></a><span data-ttu-id="edd9b-263">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-263">Parameters</span></span>

<span data-ttu-id="edd9b-264">テーブル</span><span class="sxs-lookup"><span data-stu-id="edd9b-264">table</span></span>  

<!-- -->

<span data-ttu-id="edd9b-265">名前</span><span class="sxs-lookup"><span data-stu-id="edd9b-265">name</span></span>  

<!-- -->

<span data-ttu-id="edd9b-266">unionType</span><span class="sxs-lookup"><span data-stu-id="edd9b-266">unionType</span></span>  

<!-- -->

<span data-ttu-id="edd9b-267">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="edd9b-267">emptyFieldList</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-268">Return Value</span></span>

<span data-ttu-id="edd9b-269">作成されたデータ ソース オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="edd9b-269">The data source object that is created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-270">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-270">Remarks</span></span>

<span data-ttu-id="edd9b-271">文書作成のために名前の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-271">A name value can be specified for documentation purposes.</span></span> <span data-ttu-id="edd9b-272">dataSourceName メソッドを使用してデータ ソースをフェッチする名前を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-272">You can use the name to fetch the data source by using the dataSourceName method.</span></span>

### <a name="method-addhavingfilter"></a><span data-ttu-id="edd9b-273">メソッド addHavingFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-273">Method addHavingFilter</span></span>

    public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-274">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-274">Parameters</span></span>

<span data-ttu-id="edd9b-275">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-275">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-276">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-276">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-277">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="edd9b-277">aggregateFunction</span></span>  

<!-- -->

<span data-ttu-id="edd9b-278">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-278">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-279">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-279">Return Value</span></span>

### <a name="method-addqueryfilter"></a><span data-ttu-id="edd9b-280">メソッド addQueryFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-280">Method addQueryFilter</span></span>

    public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-281">Parameters</span></span>

<span data-ttu-id="edd9b-282">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-282">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-283">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-283">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-284">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-284">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-285">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-285">Return Value</span></span>

### <a name="method-allowcheck"></a><span data-ttu-id="edd9b-286">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="edd9b-286">Method allowCheck</span></span>

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-287">Parameters</span></span>

<span data-ttu-id="edd9b-288">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-288">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-289">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-289">Return Value</span></span>

### <a name="method-allowcrosscompany"></a><span data-ttu-id="edd9b-290">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="edd9b-290">Method allowCrossCompany</span></span>

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-291">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-291">Parameters</span></span>

<span data-ttu-id="edd9b-292">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-292">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-293">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-293">Return Value</span></span>

### <a name="method-allowhavingfilters"></a><span data-ttu-id="edd9b-294">メソッド allowHavingFilters</span><span class="sxs-lookup"><span data-stu-id="edd9b-294">Method allowHavingFilters</span></span>

    public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)

#### <a name="parameters"></a><span data-ttu-id="edd9b-295">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-295">Parameters</span></span>

<span data-ttu-id="edd9b-296">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-296">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-297">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-297">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-298">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="edd9b-298">aggregateFunction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-299">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-299">Return Value</span></span>

### <a name="method-allowqueryfilters"></a><span data-ttu-id="edd9b-300">メソッド allowQueryFilters</span><span class="sxs-lookup"><span data-stu-id="edd9b-300">Method allowQueryFilters</span></span>

    public boolean allowQueryFilters(QueryBuildDataSource dataSource)

#### <a name="parameters"></a><span data-ttu-id="edd9b-301">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-301">Parameters</span></span>

<span data-ttu-id="edd9b-302">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-302">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-303">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-303">Return Value</span></span>

### <a name="method-changedby"></a><span data-ttu-id="edd9b-304">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-304">Method changedBy</span></span>

<span data-ttu-id="edd9b-305">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-305">Gets or sets the name of the user who last changed the Query object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-306">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-306">Parameters</span></span>

<span data-ttu-id="edd9b-307">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-307">value</span></span>  
<span data-ttu-id="edd9b-308">クエリ オブジェクトを最後に変更したユーザーの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-308">The name of the user who last changed the Query object; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-309">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-309">Return Value</span></span>

<span data-ttu-id="edd9b-310">クエリ オブジェクトを最後に変更したユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-310">The name of the user who last changed the Query object.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="edd9b-311">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-311">Method changedDate</span></span>

<span data-ttu-id="edd9b-312">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-312">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-313">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-313">Parameters</span></span>

<span data-ttu-id="edd9b-314">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-314">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-315">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-315">Return Value</span></span>

<span data-ttu-id="edd9b-316">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="edd9b-316">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="edd9b-317">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-317">Method changedTime</span></span>

<span data-ttu-id="edd9b-318">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-318">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-319">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-319">Parameters</span></span>

<span data-ttu-id="edd9b-320">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-320">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-321">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-321">Return Value</span></span>

<span data-ttu-id="edd9b-322">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="edd9b-322">The time an application object was last changed.</span></span>

### <a name="method-childdatasourcecount"></a><span data-ttu-id="edd9b-323">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-323">Method childDataSourceCount</span></span>

<span data-ttu-id="edd9b-324">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-324">Counts the number of data sources that are related to the query.</span></span>

    public int childDataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-325">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-325">Return Value</span></span>

<span data-ttu-id="edd9b-326">このクエリに関連するデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="edd9b-326">The number of data sources that are related to the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-327">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-327">Remarks</span></span>

<span data-ttu-id="edd9b-328">このメソッドは、トップレベルのクエリに使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-328">This method is used for the top-level query.</span></span> <span data-ttu-id="edd9b-329">別のデータ ソースに埋め込まれているデータ ソースの数を確認するには、childDataSourceCount メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-329">To determine the number of data sources that are embedded in another data source, use the childDataSourceCount method.</span></span>

### <a name="method-childdatasourceno"></a><span data-ttu-id="edd9b-330">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-330">Method childDataSourceNo</span></span>

<span data-ttu-id="edd9b-331">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-331">Returns the child data source that corresponds to the specified number.</span></span>

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-332">Parameters</span></span>

<span data-ttu-id="edd9b-333">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-333">dataSourceNo</span></span>  
<span data-ttu-id="edd9b-334">子データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-334">The number of the child data source.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-335">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-335">Return Value</span></span>

<span data-ttu-id="edd9b-336">指定された番号を持つ子データ ソース。</span><span class="sxs-lookup"><span data-stu-id="edd9b-336">The child data source that has the specified number.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-337">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-337">Remarks</span></span>

<span data-ttu-id="edd9b-338">指定された数値は、クエリのすぐ下にあるデータ ソースを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-338">The number that is specified must represent a data source that is immediately underneath the query.</span></span> <span data-ttu-id="edd9b-339">通常、このようなデータ ソースは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="edd9b-339">Typically, there is only one such data source.</span></span>

### <a name="method-containsaggregatefields"></a><span data-ttu-id="edd9b-340">メソッド containsAggregateFields</span><span class="sxs-lookup"><span data-stu-id="edd9b-340">Method containsAggregateFields</span></span>

    public boolean containsAggregateFields()

#### <a name="return-value"></a><span data-ttu-id="edd9b-341">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-341">Return Value</span></span>

### <a name="method-createdby"></a><span data-ttu-id="edd9b-342">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-342">Method createdBy</span></span>

<span data-ttu-id="edd9b-343">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-343">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-344">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-344">Parameters</span></span>

<span data-ttu-id="edd9b-345">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-345">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-346">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-346">Return Value</span></span>

<span data-ttu-id="edd9b-347">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-347">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="edd9b-348">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-348">Method creationDate</span></span>

<span data-ttu-id="edd9b-349">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-349">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-350">Parameters</span></span>

<span data-ttu-id="edd9b-351">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-351">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-352">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-352">Return Value</span></span>

<span data-ttu-id="edd9b-353">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="edd9b-353">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="edd9b-354">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-354">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-355">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-355">Parameters</span></span>

<span data-ttu-id="edd9b-356">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-356">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-357">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-357">Return Value</span></span>

### <a name="method-datasourcecount"></a><span data-ttu-id="edd9b-358">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-358">Method dataSourceCount</span></span>

<span data-ttu-id="edd9b-359">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-359">Returns the total number of data sources for the query, including any embedded data sources.</span></span>

    public int dataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-360">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-360">Return Value</span></span>

<span data-ttu-id="edd9b-361">このクエリのデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="edd9b-361">The number of data sources for this query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-362">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-362">Remarks</span></span>

<span data-ttu-id="edd9b-363">この番号は、データ ソースの推移的な番号であり、任意の埋め込みデータ ソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="edd9b-363">The number is the transitive number of data sources and includes any embedded data sources.</span></span>

### <a name="method-datasourcename"></a><span data-ttu-id="edd9b-364">メソッド dataSourceName</span><span class="sxs-lookup"><span data-stu-id="edd9b-364">Method dataSourceName</span></span>

<span data-ttu-id="edd9b-365">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-365">Returns the data source that has the specified name.</span></span>

    public QueryBuildDataSource dataSourceName(str name)

#### <a name="parameters"></a><span data-ttu-id="edd9b-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-366">Parameters</span></span>

<span data-ttu-id="edd9b-367">名前</span><span class="sxs-lookup"><span data-stu-id="edd9b-367">name</span></span>  
<span data-ttu-id="edd9b-368">返すデータソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-368">The string that contains the name of the data source to return.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-369">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-369">Return Value</span></span>

<span data-ttu-id="edd9b-370">指定した名前を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="edd9b-370">The data source that has the specified name; an uninitialized object if the specified data source does not exist.</span></span>

### <a name="method-datasourceno"></a><span data-ttu-id="edd9b-371">メソッド dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-371">Method dataSourceNo</span></span>

<span data-ttu-id="edd9b-372">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-372">Returns the data source that is specified by the data source number.</span></span>

    public QueryBuildDataSource dataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-373">Parameters</span></span>

<span data-ttu-id="edd9b-374">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-374">dataSourceNo</span></span>  
<span data-ttu-id="edd9b-375">データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-375">The number of the data source.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-376">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-376">Return Value</span></span>

<span data-ttu-id="edd9b-377">指定した番号を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="edd9b-377">The data source that has the specified number; an uninitialized object if the specified data source does not exist.</span></span>

### <a name="method-datasourcetable"></a><span data-ttu-id="edd9b-378">メソッド dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="edd9b-378">Method dataSourceTable</span></span>

<span data-ttu-id="edd9b-379">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-379">Returns the data source that the specified table is assigned to.</span></span>

    public QueryBuildDataSource dataSourceTable(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-380">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-380">Parameters</span></span>

<span data-ttu-id="edd9b-381">テーブル</span><span class="sxs-lookup"><span data-stu-id="edd9b-381">table</span></span>  
<span data-ttu-id="edd9b-382">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-382">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="edd9b-383">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-383">The default value is 1, which specifies the first (and typically only) instance.</span></span>

<!-- -->

<span data-ttu-id="edd9b-384">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-384">occurrence</span></span>  
<span data-ttu-id="edd9b-385">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-385">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="edd9b-386">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-386">The default value is 1, which specifies the first (and typically only) instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-387">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-387">Return Value</span></span>

<span data-ttu-id="edd9b-388">指定されたテーブルが割り当てられているデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="edd9b-388">The data source that the specified table is assigned to.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-389">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-389">Remarks</span></span>

<span data-ttu-id="edd9b-390">データ ソースは、dataSourceNo メソッドまたは dataSourceName メソッドを呼び出すことによって取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-390">The data source can also be retrieved by calling the dataSourceNo method or the dataSourceName method.</span></span>

### <a name="method-datasourceuniqueid"></a><span data-ttu-id="edd9b-391">メソッド dataSourceUniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-391">Method dataSourceUniqueId</span></span>

    public QueryBuildDataSource dataSourceUniqueId(int uniqueId)

#### <a name="parameters"></a><span data-ttu-id="edd9b-392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-392">Parameters</span></span>

<span data-ttu-id="edd9b-393">uniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-393">uniqueId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-394">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-394">Return Value</span></span>

### <a name="method-description"></a><span data-ttu-id="edd9b-395">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-395">Method description</span></span>

    public str description([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-396">Parameters</span></span>

<span data-ttu-id="edd9b-397">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-397">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-398">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-398">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="edd9b-399">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="edd9b-399">Method equal</span></span>

<span data-ttu-id="edd9b-400">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-400">Evaluates whether one query is equal to another.</span></span>

    public boolean equal(Object record)

#### <a name="parameters"></a><span data-ttu-id="edd9b-401">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-401">Parameters</span></span>

<span data-ttu-id="edd9b-402">記録</span><span class="sxs-lookup"><span data-stu-id="edd9b-402">record</span></span>  
<span data-ttu-id="edd9b-403">比較として使用するクエリです。</span><span class="sxs-lookup"><span data-stu-id="edd9b-403">The query to use as a comparison.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-404">Return Value</span></span>

<span data-ttu-id="edd9b-405">クエリが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-405">true if the queries are equal; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-406">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-406">Remarks</span></span>

<span data-ttu-id="edd9b-407">この場合、「等しい」は、クエリが比較されるクエリと構造的に同一であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-407">"Equal" in this case means that the query is structurally identical to the query that it is compared to.</span></span> <span data-ttu-id="edd9b-408">クエリには、同じファイルに割り当てられたデータ ソースと同じ数のデータ ソースがあり、同じ数の範囲があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-408">The query has the same number of data sources assigned to the same files, and it has the same number of ranges.</span></span>

### <a name="method-exportxml"></a><span data-ttu-id="edd9b-409">メソッド exportXML</span><span class="sxs-lookup"><span data-stu-id="edd9b-409">Method exportXML</span></span>

    public str exportXML()

#### <a name="return-value"></a><span data-ttu-id="edd9b-410">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-410">Return Value</span></span>

### <a name="method-findhavingfilterbyfield"></a><span data-ttu-id="edd9b-411">メソッド findHavingFilterByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-411">Method findHavingFilterByField</span></span>

    public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-412">Parameters</span></span>

<span data-ttu-id="edd9b-413">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-413">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-414">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-414">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-415">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-415">occurrence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-416">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-416">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-417">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-417">Return Value</span></span>

### <a name="method-findqueryfilter"></a><span data-ttu-id="edd9b-418">メソッド findQueryFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-418">Method findQueryFilter</span></span>

    public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-419">Parameters</span></span>

<span data-ttu-id="edd9b-420">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-420">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-421">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-421">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-422">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-422">occurrence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-423">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-423">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-424">Return Value</span></span>

### <a name="method-firsttopleveldatasource"></a><span data-ttu-id="edd9b-425">メソッド firstTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-425">Method firstTopLevelDataSource</span></span>

    public QueryBuildDataSource firstTopLevelDataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-426">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-426">Return Value</span></span>

### <a name="method-forcenestedloop"></a><span data-ttu-id="edd9b-427">メソッド forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="edd9b-427">Method forceNestedLoop</span></span>

    public boolean forceNestedLoop(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="edd9b-428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-428">Parameters</span></span>

<span data-ttu-id="edd9b-429">arg</span><span class="sxs-lookup"><span data-stu-id="edd9b-429">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-430">Return Value</span></span>

### <a name="method-forceselectorder"></a><span data-ttu-id="edd9b-431">メソッド forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="edd9b-431">Method forceSelectOrder</span></span>

    public boolean forceSelectOrder(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="edd9b-432">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-432">Parameters</span></span>

<span data-ttu-id="edd9b-433">arg</span><span class="sxs-lookup"><span data-stu-id="edd9b-433">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-434">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-434">Return Value</span></span>

### <a name="method-form"></a><span data-ttu-id="edd9b-435">メソッド form</span><span class="sxs-lookup"><span data-stu-id="edd9b-435">Method form</span></span>

    public str form([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-436">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-436">Parameters</span></span>

<span data-ttu-id="edd9b-437">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-437">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-438">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-438">Return Value</span></span>

### <a name="method-getcompanyrange"></a><span data-ttu-id="edd9b-439">メソッド getCompanyRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-439">Method getCompanyRange</span></span>

    public container getCompanyRange()

#### <a name="return-value"></a><span data-ttu-id="edd9b-440">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-440">Return Value</span></span>

### <a name="method-getmostrestrictedqueryfilterstatus"></a><span data-ttu-id="edd9b-441">メソッド getMostRestrictedQueryFilterStatus</span><span class="sxs-lookup"><span data-stu-id="edd9b-441">Method getMostRestrictedQueryFilterStatus</span></span>

    public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, [int fieldId])

#### <a name="parameters"></a><span data-ttu-id="edd9b-442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-442">Parameters</span></span>

<span data-ttu-id="edd9b-443">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-443">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-444">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-444">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-445">fieldId</span><span class="sxs-lookup"><span data-stu-id="edd9b-445">fieldId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-446">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-446">Return Value</span></span>

### <a name="method-getnextuniqueid"></a><span data-ttu-id="edd9b-447">メソッド getNextUniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-447">Method getNextUniqueId</span></span>

    public int getNextUniqueId()

#### <a name="return-value"></a><span data-ttu-id="edd9b-448">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-448">Return Value</span></span>

### <a name="method-getsqlstatement"></a><span data-ttu-id="edd9b-449">メソッド getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="edd9b-449">Method getSQLStatement</span></span>

    public str getSQLStatement([boolean noRuntimeOptimization])

#### <a name="parameters"></a><span data-ttu-id="edd9b-450">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-450">Parameters</span></span>

<span data-ttu-id="edd9b-451">noRuntimeOptimization</span><span class="sxs-lookup"><span data-stu-id="edd9b-451">noRuntimeOptimization</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-452">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-452">Return Value</span></span>

### <a name="method-getvalidtimestatedaterange"></a><span data-ttu-id="edd9b-453">メソッド getValidTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-453">Method getValidTimeStateDateRange</span></span>

    public container getValidTimeStateDateRange()

#### <a name="return-value"></a><span data-ttu-id="edd9b-454">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-454">Return Value</span></span>

### <a name="method-getvalidtimestatedatetimerange"></a><span data-ttu-id="edd9b-455">メソッド getValidTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-455">Method getValidTimeStateDateTimeRange</span></span>

    public container getValidTimeStateDateTimeRange()

#### <a name="return-value"></a><span data-ttu-id="edd9b-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-456">Return Value</span></span>

### <a name="method-getvalidtimestatequerytype"></a><span data-ttu-id="edd9b-457">メソッド getValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="edd9b-457">Method getValidTimeStateQueryType</span></span>

    public ValidTimeStateQueryType getValidTimeStateQueryType()

#### <a name="return-value"></a><span data-ttu-id="edd9b-458">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-458">Return Value</span></span>

### <a name="method-groupbyfield"></a><span data-ttu-id="edd9b-459">メソッド groupByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-459">Method groupByField</span></span>

    public QueryGroupByField groupByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-460">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-460">Parameters</span></span>

<span data-ttu-id="edd9b-461">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-461">index</span></span>  

<!-- -->

<span data-ttu-id="edd9b-462">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-462">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-463">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-463">Return Value</span></span>

### <a name="method-groupbyfieldcount"></a><span data-ttu-id="edd9b-464">メソッド groupByFieldCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-464">Method groupByFieldCount</span></span>

    public int groupByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-465">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-465">Parameters</span></span>

<span data-ttu-id="edd9b-466">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-466">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-467">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-467">Return Value</span></span>

### <a name="method-hasmultipletopleveldatasource"></a><span data-ttu-id="edd9b-468">メソッド hasMultipleTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-468">Method hasMultipleTopLevelDataSource</span></span>

    public boolean hasMultipleTopLevelDataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-469">Return Value</span></span>

### <a name="method-hasrangeorfilter"></a><span data-ttu-id="edd9b-470">メソッド hasRangeOrFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-470">Method hasRangeOrFilter</span></span>

    public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)

#### <a name="parameters"></a><span data-ttu-id="edd9b-471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-471">Parameters</span></span>

<span data-ttu-id="edd9b-472">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-472">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-473">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-473">Return Value</span></span>

### <a name="method-havingfilter"></a><span data-ttu-id="edd9b-474">メソッド havingFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-474">Method havingFilter</span></span>

    public QueryHavingFilter havingFilter(int count, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-475">Parameters</span></span>

<span data-ttu-id="edd9b-476">カウント</span><span class="sxs-lookup"><span data-stu-id="edd9b-476">count</span></span>  

<!-- -->

<span data-ttu-id="edd9b-477">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-477">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-478">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-478">Return Value</span></span>

### <a name="method-havingfiltercount"></a><span data-ttu-id="edd9b-479">メソッド havingFilterCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-479">Method havingFilterCount</span></span>

    public int havingFilterCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-480">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-480">Parameters</span></span>

<span data-ttu-id="edd9b-481">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-481">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-482">Return Value</span></span>

### <a name="method-inreport"></a><span data-ttu-id="edd9b-483">メソッド inReport</span><span class="sxs-lookup"><span data-stu-id="edd9b-483">Method inReport</span></span>

<span data-ttu-id="edd9b-484">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-484">Determines whether the query is part of a report.</span></span>

    public boolean inReport()

#### <a name="return-value"></a><span data-ttu-id="edd9b-485">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-485">Return Value</span></span>

<span data-ttu-id="edd9b-486">クエリがレポートの一部である場合は (レポートのデータ ソース ノードの下にある場合は) true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-486">true if the query is part of a report (is found under a report's data sources node); otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-487">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-487">Remarks</span></span>

<span data-ttu-id="edd9b-488">この関数は、通常アプリケーション コードでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-488">This function is not typically used by application code.</span></span> <span data-ttu-id="edd9b-489">メソッドが true を返す場合は、レポート メソッドはクエリが定義されているレポートにアクセスするために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-489">If the method returns true, the report method can be used to access the report in which the query is defined.</span></span>

### <a name="method-interactive"></a><span data-ttu-id="edd9b-490">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="edd9b-490">Method interactive</span></span>

<span data-ttu-id="edd9b-491">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-491">Specifies whether the query is interactive.</span></span>

    public boolean interactive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-492">Parameters</span></span>

<span data-ttu-id="edd9b-493">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-493">value</span></span>  
<span data-ttu-id="edd9b-494">クエリがインタラクティブかどうかを示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-494">A value that indicates whether the query is interactive; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-495">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-495">Return Value</span></span>

<span data-ttu-id="edd9b-496">クエリが対話形式である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-496">true if the query is interactive; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-497">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-497">Remarks</span></span>

<span data-ttu-id="edd9b-498">対話型クエリでは、たとえば prompt メソッドが呼び出されたときに、クエリはユーザーにダイアログ ボックスを提示できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-498">In an interactive query, the query can, for example, present the user with a dialog box when the prompt method is called.</span></span> <span data-ttu-id="edd9b-499">この機能は、コードをバッチに送信する場合や、コードを無人で実行する必要がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-499">This functionality is used when code will be submitted to a batch and in other situations where code must run unattended.</span></span>

### <a name="method-iscompositequery"></a><span data-ttu-id="edd9b-500">メソッド isCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-500">Method isCompositeQuery</span></span>

    public boolean isCompositeQuery()

#### <a name="return-value"></a><span data-ttu-id="edd9b-501">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-501">Return Value</span></span>

### <a name="method-isexplicitlyordered"></a><span data-ttu-id="edd9b-502">メソッド isExplicitlyOrdered</span><span class="sxs-lookup"><span data-stu-id="edd9b-502">Method isExplicitlyOrdered</span></span>

    public boolean isExplicitlyOrdered()

#### <a name="return-value"></a><span data-ttu-id="edd9b-503">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-503">Return Value</span></span>

### <a name="method-isexplicitlygrouped"></a><span data-ttu-id="edd9b-504">メソッド isExplicitlyGrouped</span><span class="sxs-lookup"><span data-stu-id="edd9b-504">Method isExplicitlyGrouped</span></span>

    public boolean isExplicitlyGrouped()

#### <a name="return-value"></a><span data-ttu-id="edd9b-505">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-505">Return Value</span></span>

### <a name="method-ispureunionall"></a><span data-ttu-id="edd9b-506">メソッド isPureUnionAll</span><span class="sxs-lookup"><span data-stu-id="edd9b-506">Method isPureUnionAll</span></span>

    public boolean isPureUnionAll()

#### <a name="return-value"></a><span data-ttu-id="edd9b-507">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-507">Return Value</span></span>

### <a name="method-isuniontype"></a><span data-ttu-id="edd9b-508">メソッド isUnionType</span><span class="sxs-lookup"><span data-stu-id="edd9b-508">Method isUnionType</span></span>

    public boolean isUnionType()

#### <a name="return-value"></a><span data-ttu-id="edd9b-509">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-509">Return Value</span></span>

### <a name="method-levelno"></a><span data-ttu-id="edd9b-510">メソッド levelNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-510">Method levelNo</span></span>

<span data-ttu-id="edd9b-511">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-511">Determines the level of indentation of the specified data source.</span></span>

    public int levelNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-512">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-512">Parameters</span></span>

<span data-ttu-id="edd9b-513">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-513">dataSourceNo</span></span>  
<span data-ttu-id="edd9b-514">データ ソースのレベルを決定する番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-514">The data source number to determine the level for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-515">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-515">Return Value</span></span>

<span data-ttu-id="edd9b-516">指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-516">The level number of the specified data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-517">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-517">Remarks</span></span>

<span data-ttu-id="edd9b-518">データソースは、1 から順に番号付けされます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-518">The data sources are numbered consecutively, starting at 1.</span></span>

### <a name="method-leveltable"></a><span data-ttu-id="edd9b-519">メソッド levelTable</span><span class="sxs-lookup"><span data-stu-id="edd9b-519">Method levelTable</span></span>

<span data-ttu-id="edd9b-520">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-520">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>

    public int levelTable(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-521">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-521">Parameters</span></span>

<span data-ttu-id="edd9b-522">テーブル</span><span class="sxs-lookup"><span data-stu-id="edd9b-522">table</span></span>  
<span data-ttu-id="edd9b-523">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-523">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

<!-- -->

<span data-ttu-id="edd9b-524">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-524">occurrence</span></span>  
<span data-ttu-id="edd9b-525">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-525">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-526">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-526">Return Value</span></span>

<span data-ttu-id="edd9b-527">クエリの指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-527">The level number of the query's specified data source.</span></span>

### <a name="method-literals"></a><span data-ttu-id="edd9b-528">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="edd9b-528">Method literals</span></span>

    public int literals([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-529">Parameters</span></span>

<span data-ttu-id="edd9b-530">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-530">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-531">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-531">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="edd9b-532">メソッド名</span><span class="sxs-lookup"><span data-stu-id="edd9b-532">Method name</span></span>

<span data-ttu-id="edd9b-533">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-533">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-534">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-534">Parameters</span></span>

<span data-ttu-id="edd9b-535">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-535">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-536">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-536">Return Value</span></span>

<span data-ttu-id="edd9b-537">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-537">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-538">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-538">Remarks</span></span>

<span data-ttu-id="edd9b-539">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-539">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="edd9b-540">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-540">Begins with a letter.</span></span>
-   <span data-ttu-id="edd9b-541">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-541">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="edd9b-542">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-542">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="edd9b-543">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-543">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="edd9b-544">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-544">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-newobject"></a><span data-ttu-id="edd9b-545">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="edd9b-545">Method newObject</span></span>

<span data-ttu-id="edd9b-546">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-546">Creates a query that exists on the same client side or server side as the source query.</span></span>

    public Query newObject(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="edd9b-547">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-547">Parameters</span></span>

<span data-ttu-id="edd9b-548">ソース</span><span class="sxs-lookup"><span data-stu-id="edd9b-548">source</span></span>  
<span data-ttu-id="edd9b-549">ソース クエリ。</span><span class="sxs-lookup"><span data-stu-id="edd9b-549">The source query.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-550">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-550">Return Value</span></span>

<span data-ttu-id="edd9b-551">新しいクエリ。</span><span class="sxs-lookup"><span data-stu-id="edd9b-551">The new query.</span></span>

### <a name="method-nextuniqueid"></a><span data-ttu-id="edd9b-552">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-552">Method nextUniqueId</span></span>

    public int nextUniqueId([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-553">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-553">Parameters</span></span>

<span data-ttu-id="edd9b-554">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-554">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-555">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-555">Return Value</span></span>

### <a name="method-orderbyfield"></a><span data-ttu-id="edd9b-556">メソッド orderByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-556">Method orderByField</span></span>

    public QueryOrderByField orderByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-557">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-557">Parameters</span></span>

<span data-ttu-id="edd9b-558">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-558">index</span></span>  

<!-- -->

<span data-ttu-id="edd9b-559">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-559">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-560">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-560">Return Value</span></span>

### <a name="method-orderbyfieldcount"></a><span data-ttu-id="edd9b-561">メソッド orderByFieldCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-561">Method orderByFieldCount</span></span>

    public int orderByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-562">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-562">Parameters</span></span>

<span data-ttu-id="edd9b-563">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-563">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-564">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-564">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="edd9b-565">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="edd9b-565">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-566">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-566">Parameters</span></span>

<span data-ttu-id="edd9b-567">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-567">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-568">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-568">Return Value</span></span>

### <a name="method-pack"></a><span data-ttu-id="edd9b-569">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="edd9b-569">Method pack</span></span>

<span data-ttu-id="edd9b-570">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-570">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>

    public container pack([boolean doCheck])

#### <a name="parameters"></a><span data-ttu-id="edd9b-571">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-571">Parameters</span></span>

<span data-ttu-id="edd9b-572">doCheck</span><span class="sxs-lookup"><span data-stu-id="edd9b-572">doCheck</span></span>  
<span data-ttu-id="edd9b-573">クエリのデーターソースが外部のカーソルを参照する (クエリのデータソースを外部のカーソルへリンクするなど) ときに、エラーフラグを設定するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-573">A Boolean value that indicates whether to flag an error when a data source in the query references an outside cursor, such as a link to a cursor that is foreign to the query's data source; optional.</span></span> <span data-ttu-id="edd9b-574">既定値は、true で、制約が適用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-574">The default value is true, which enforces the constraint.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-575">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-575">Return Value</span></span>

<span data-ttu-id="edd9b-576">クエリを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="edd9b-576">The container that holds the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-577">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-577">Remarks</span></span>

<span data-ttu-id="edd9b-578">このメソッドで作成されたコンテナーは、新しいメソッドまたは newObject メソッドのいずれかを使用して query オブジェクトまたは queryRun オブジェクトをインスタンス化するときに入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-578">The container that is created by this method can serve as input when you instantiate a query or queryRun object by using either the new method or the newObject method.</span></span> <span data-ttu-id="edd9b-579">クエリのデータ ソースとは異なるカーソルへのリンクは、コンテナーにパックされません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-579">Links to cursors that are foreign to the query's data source are not packed into the container.</span></span> <span data-ttu-id="edd9b-580">この種類のリンクをパックする必要がある場合は、カーソルのデータのスナップショットを取得し、各フィールドの範囲を作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-580">If you must pack this kind of link, you should take a snapshot of the cursor's data and construct ranges for each field.</span></span>

### <a name="method-packinternals"></a><span data-ttu-id="edd9b-581">メソッド packInternals</span><span class="sxs-lookup"><span data-stu-id="edd9b-581">Method packInternals</span></span>

    public container packInternals()

#### <a name="return-value"></a><span data-ttu-id="edd9b-582">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-582">Return Value</span></span>

### <a name="method-queryfilter"></a><span data-ttu-id="edd9b-583">メソッド queryFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-583">Method queryFilter</span></span>

    public QueryFilter queryFilter(int count, [QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-584">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-584">Parameters</span></span>

<span data-ttu-id="edd9b-585">カウント</span><span class="sxs-lookup"><span data-stu-id="edd9b-585">count</span></span>  

<!-- -->

<span data-ttu-id="edd9b-586">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-586">rootDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-587">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-587">Return Value</span></span>

### <a name="method-queryfiltercount"></a><span data-ttu-id="edd9b-588">メソッド queryFilterCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-588">Method queryFilterCount</span></span>

    public int queryFilterCount([QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a><span data-ttu-id="edd9b-589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-589">Parameters</span></span>

<span data-ttu-id="edd9b-590">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-590">rootDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-591">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-591">Return Value</span></span>

### <a name="method-querytype"></a><span data-ttu-id="edd9b-592">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="edd9b-592">Method queryType</span></span>

    public int queryType([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-593">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-593">Parameters</span></span>

<span data-ttu-id="edd9b-594">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-594">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-595">Return Value</span></span>

### <a name="method-quickfiltervalue"></a><span data-ttu-id="edd9b-596">メソッド quickFilterValue</span><span class="sxs-lookup"><span data-stu-id="edd9b-596">Method quickFilterValue</span></span>

    public str quickFilterValue()

#### <a name="return-value"></a><span data-ttu-id="edd9b-597">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-597">Return Value</span></span>

### <a name="method-quickfiltercontrolid"></a><span data-ttu-id="edd9b-598">メソッド quickFilterControlId</span><span class="sxs-lookup"><span data-stu-id="edd9b-598">Method quickFilterControlId</span></span>

    public int quickFilterControlId()

#### <a name="return-value"></a><span data-ttu-id="edd9b-599">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-599">Return Value</span></span>

### <a name="method-recordlevelsecurity"></a><span data-ttu-id="edd9b-600">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="edd9b-600">Method recordLevelSecurity</span></span>

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-601">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-601">Parameters</span></span>

<span data-ttu-id="edd9b-602">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-602">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-603">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-603">Return Value</span></span>

### <a name="method-report"></a><span data-ttu-id="edd9b-604">メソッド report</span><span class="sxs-lookup"><span data-stu-id="edd9b-604">Method report</span></span>

<span data-ttu-id="edd9b-605">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-605">Returns the report in which the query is defined, if the report exists.</span></span>

    public Report report()

#### <a name="return-value"></a><span data-ttu-id="edd9b-606">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-606">Return Value</span></span>

<span data-ttu-id="edd9b-607">クエリがデータ ソース ノードの下で定義されているレポート。</span><span class="sxs-lookup"><span data-stu-id="edd9b-607">The report in which the query is defined under the data sources node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-608">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-608">Remarks</span></span>

<span data-ttu-id="edd9b-609">クエリは、必ずしもレポートのコンテキストで定義されているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-609">A query is not necessarily defined in the context of a report.</span></span> <span data-ttu-id="edd9b-610">レポートのコンテキストでクエリが定義されているかどうかを確認するには、inReport メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-610">To determine whether a query is defined in the context of a report, you can use the inReport method.</span></span>

### <a name="method-saved"></a><span data-ttu-id="edd9b-611">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="edd9b-611">Method saved</span></span>

<span data-ttu-id="edd9b-612">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-612">Indicates whether the query has been saved to disk.</span></span>

    public boolean saved()

#### <a name="return-value"></a><span data-ttu-id="edd9b-613">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-613">Return Value</span></span>

<span data-ttu-id="edd9b-614">クエリがディスクに保存されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-614">true if the query has been saved to disk; otherwise, false.</span></span>

### <a name="method-searchable"></a><span data-ttu-id="edd9b-615">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="edd9b-615">Method searchable</span></span>

    public boolean searchable([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-616">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-616">Parameters</span></span>

<span data-ttu-id="edd9b-617">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-617">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-618">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-618">Return Value</span></span>

### <a name="method-importsession"></a><span data-ttu-id="edd9b-619">メソッド importSession</span><span class="sxs-lookup"><span data-stu-id="edd9b-619">Method importSession</span></span>

    public Guid importSession([Guid value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-620">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-620">Parameters</span></span>

<span data-ttu-id="edd9b-621">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-621">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-622">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-622">Return Value</span></span>

### <a name="method-title"></a><span data-ttu-id="edd9b-623">メソッド title</span><span class="sxs-lookup"><span data-stu-id="edd9b-623">Method title</span></span>

    public str title([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-624">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-624">Parameters</span></span>

<span data-ttu-id="edd9b-625">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-625">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-626">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-626">Return Value</span></span>

### <a name="method-toprows"></a><span data-ttu-id="edd9b-627">メソッド topRows</span><span class="sxs-lookup"><span data-stu-id="edd9b-627">Method topRows</span></span>

    public int topRows([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-628">Parameters</span></span>

<span data-ttu-id="edd9b-629">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-629">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-630">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-630">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-631">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-631">Method toString</span></span>

<span data-ttu-id="edd9b-632">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-632">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-633">Return Value</span></span>

<span data-ttu-id="edd9b-634">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-634">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-635">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-635">Remarks</span></span>

<span data-ttu-id="edd9b-636">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-636">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-637">ただし、メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-637">However, the method can be overridden in a derived class so that it returns values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-638">たとえば、SysMethodInfo クラスのインスタンスは、メソッド名、およびインスタンスまたは静的などのメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-638">For example, an instance of the SysMethodInfo class returns the method name, and the type of method, such as Instance or Static.</span></span>

### <a name="method-userupdate"></a><span data-ttu-id="edd9b-639">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="edd9b-639">Method userUpdate</span></span>

<span data-ttu-id="edd9b-640">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-640">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-641">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-641">Parameters</span></span>

<span data-ttu-id="edd9b-642">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-642">value</span></span>  
<span data-ttu-id="edd9b-643">フェッチされたレコードをクエリが更新できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="edd9b-643">A Boolean value that indicates whether the query can update the records that it fetches; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-644">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-644">Return Value</span></span>

<span data-ttu-id="edd9b-645">クエリがフェッチ対象のレコードを現在更新することができる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-645">true if the query can currently update records that it fetches; otherwise false.</span></span>

### <a name="method-validtimestateasofdate"></a><span data-ttu-id="edd9b-646">メソッド validTimeStateAsOfDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-646">Method validTimeStateAsOfDate</span></span>

    public Date validTimeStateAsOfDate([Date asOfDate])

#### <a name="parameters"></a><span data-ttu-id="edd9b-647">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-647">Parameters</span></span>

<span data-ttu-id="edd9b-648">asOfDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-648">asOfDate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-649">Return Value</span></span>

### <a name="method-validtimestateasofdatetime"></a><span data-ttu-id="edd9b-650">メソッド validTimeStateAsOfDateTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-650">Method validTimeStateAsOfDateTime</span></span>

    public DateTime validTimeStateAsOfDateTime([DateTime asOfDateTime])

#### <a name="parameters"></a><span data-ttu-id="edd9b-651">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-651">Parameters</span></span>

<span data-ttu-id="edd9b-652">asOfDateTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-652">asOfDateTime</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-653">Return Value</span></span>

### <a name="method-validtimestateflags"></a><span data-ttu-id="edd9b-654">メソッド validTimeStateFlags</span><span class="sxs-lookup"><span data-stu-id="edd9b-654">Method validTimeStateFlags</span></span>

    public int validTimeStateFlags([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-655">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-655">Parameters</span></span>

<span data-ttu-id="edd9b-656">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-656">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-657">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="edd9b-658">メソッド version</span><span class="sxs-lookup"><span data-stu-id="edd9b-658">Method version</span></span>

    public int version([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-659">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-659">Parameters</span></span>

<span data-ttu-id="edd9b-660">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-660">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-661">Return Value</span></span>

### <a name="method-xml"></a><span data-ttu-id="edd9b-662">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="edd9b-662">Method xml</span></span>

<span data-ttu-id="edd9b-663">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-663">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="edd9b-664">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-664">Parameters</span></span>

<span data-ttu-id="edd9b-665">インデント</span><span class="sxs-lookup"><span data-stu-id="edd9b-665">indent</span></span>  
<span data-ttu-id="edd9b-666">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-666">The amount of indentation for the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-667">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-667">Return Value</span></span>

<span data-ttu-id="edd9b-668">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-668">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-669">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-669">Remarks</span></span>

<span data-ttu-id="edd9b-670">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-670">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-clearbasequeries"></a><span data-ttu-id="edd9b-671">メソッド clearBaseQueries</span><span class="sxs-lookup"><span data-stu-id="edd9b-671">Method clearBaseQueries</span></span>

    public void clearBaseQueries()

### <a name="method-addcompanyrange"></a><span data-ttu-id="edd9b-672">メソッド addCompanyRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-672">Method addCompanyRange</span></span>

    public void addCompanyRange(str companyName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-673">Parameters</span></span>

<span data-ttu-id="edd9b-674">companyName</span><span class="sxs-lookup"><span data-stu-id="edd9b-674">companyName</span></span>  

### <a name="method-checkrangeparsingerrors"></a><span data-ttu-id="edd9b-675">メソッド checkRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="edd9b-675">Method checkRangeParsingErrors</span></span>

    public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)

#### <a name="parameters"></a><span data-ttu-id="edd9b-676">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-676">Parameters</span></span>

<span data-ttu-id="edd9b-677">setCheckRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="edd9b-677">setCheckRangeParsingErrors</span></span>  

### <a name="method-clearcompanyrange"></a><span data-ttu-id="edd9b-678">メソッド clearCompanyRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-678">Method clearCompanyRange</span></span>

    public void clearCompanyRange()

### <a name="method-unpackinternals"></a><span data-ttu-id="edd9b-679">メソッド unpackInternals</span><span class="sxs-lookup"><span data-stu-id="edd9b-679">Method unpackInternals</span></span>

    public void unpackInternals(container internalData)

#### <a name="parameters"></a><span data-ttu-id="edd9b-680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-680">Parameters</span></span>

<span data-ttu-id="edd9b-681">internalData</span><span class="sxs-lookup"><span data-stu-id="edd9b-681">internalData</span></span>  

### <a name="method-new"></a><span data-ttu-id="edd9b-682">メソッド new</span><span class="sxs-lookup"><span data-stu-id="edd9b-682">Method new</span></span>

<span data-ttu-id="edd9b-683">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-683">Creates a query object.</span></span>

    public void new([AnyType source])

#### <a name="parameters"></a><span data-ttu-id="edd9b-684">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-684">Parameters</span></span>

<span data-ttu-id="edd9b-685">ソース</span><span class="sxs-lookup"><span data-stu-id="edd9b-685">source</span></span>  
<span data-ttu-id="edd9b-686">クエリ オブジェクトを基にするソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-686">The source to base the query object on; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-687">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-687">Remarks</span></span>

<span data-ttu-id="edd9b-688">このメソッドが呼び出されときに引数が指定されていない場合、将来使用するために、アプリケーション オブジェクト ツリー (AOT) で保存されていない一時的なクエリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-688">If no arguments are supplied when this method is called, a temporary query is created that is not stored in the Application Object Tree (AOT) for subsequent use.</span></span>

### <a name="method-checkfieldaccess"></a><span data-ttu-id="edd9b-689">メソッド checkFieldAccess</span><span class="sxs-lookup"><span data-stu-id="edd9b-689">Method checkFieldAccess</span></span>

    public void checkFieldAccess(boolean setCheckFieldAccess)

#### <a name="parameters"></a><span data-ttu-id="edd9b-690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-690">Parameters</span></span>

<span data-ttu-id="edd9b-691">setCheckFieldAccess</span><span class="sxs-lookup"><span data-stu-id="edd9b-691">setCheckFieldAccess</span></span>  

### <a name="method-usedbcacheongeneratedcursors"></a><span data-ttu-id="edd9b-692">メソッド useDbCacheOnGeneratedCursors</span><span class="sxs-lookup"><span data-stu-id="edd9b-692">Method useDbCacheOnGeneratedCursors</span></span>

    public void useDbCacheOnGeneratedCursors([int fetchsize])

#### <a name="parameters"></a><span data-ttu-id="edd9b-693">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-693">Parameters</span></span>

<span data-ttu-id="edd9b-694">fetchsize</span><span class="sxs-lookup"><span data-stu-id="edd9b-694">fetchsize</span></span>  

### <a name="method-setvalidtimestatequerytype"></a><span data-ttu-id="edd9b-695">メソッド setValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="edd9b-695">Method setValidTimeStateQueryType</span></span>

    public void setValidTimeStateQueryType([ValidTimeStateQueryType type])

#### <a name="parameters"></a><span data-ttu-id="edd9b-696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-696">Parameters</span></span>

<span data-ttu-id="edd9b-697">タイプ</span><span class="sxs-lookup"><span data-stu-id="edd9b-697">type</span></span>  

### <a name="method-validtimestatedaterange"></a><span data-ttu-id="edd9b-698">メソッド validTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-698">Method validTimeStateDateRange</span></span>

    public void validTimeStateDateRange([Date fromDate], [Date toDate])

#### <a name="parameters"></a><span data-ttu-id="edd9b-699">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-699">Parameters</span></span>

<span data-ttu-id="edd9b-700">fromDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-700">fromDate</span></span>  

<!-- -->

<span data-ttu-id="edd9b-701">toDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-701">toDate</span></span>  

### <a name="method-clearhavingfilters"></a><span data-ttu-id="edd9b-702">メソッド clearHavingFilters</span><span class="sxs-lookup"><span data-stu-id="edd9b-702">Method clearHavingFilters</span></span>

    public void clearHavingFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-703">Parameters</span></span>

<span data-ttu-id="edd9b-704">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-704">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-705">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-705">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-706">occurence</span><span class="sxs-lookup"><span data-stu-id="edd9b-706">occurence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-707">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-707">arrayIndex</span></span>  

### <a name="method-quickfilter"></a><span data-ttu-id="edd9b-708">メソッド quickFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-708">Method quickFilter</span></span>

    public void quickFilter([str dataSourceName], [int tableId], [int fieldId], [str filterValue], [int controlId], [boolean useEqualityComparisonForStrings])

#### <a name="parameters"></a><span data-ttu-id="edd9b-709">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-709">Parameters</span></span>

<span data-ttu-id="edd9b-710">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="edd9b-710">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-711">tableId</span><span class="sxs-lookup"><span data-stu-id="edd9b-711">tableId</span></span>  

<!-- -->

<span data-ttu-id="edd9b-712">fieldId</span><span class="sxs-lookup"><span data-stu-id="edd9b-712">fieldId</span></span>  

<!-- -->

<span data-ttu-id="edd9b-713">filterValue</span><span class="sxs-lookup"><span data-stu-id="edd9b-713">filterValue</span></span>  

<!-- -->

<span data-ttu-id="edd9b-714">controlId</span><span class="sxs-lookup"><span data-stu-id="edd9b-714">controlId</span></span>  

<!-- -->

<span data-ttu-id="edd9b-715">useEqualityComparisonForStrings</span><span class="sxs-lookup"><span data-stu-id="edd9b-715">useEqualityComparisonForStrings</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="edd9b-716">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-716">Method finalize</span></span>

    public void finalize()

### <a name="method-clearqueryfilters"></a><span data-ttu-id="edd9b-717">メソッド clearQueryFilters</span><span class="sxs-lookup"><span data-stu-id="edd9b-717">Method clearQueryFilters</span></span>

    public void clearQueryFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-718">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-718">Parameters</span></span>

<span data-ttu-id="edd9b-719">dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-719">dataSource</span></span>  

<!-- -->

<span data-ttu-id="edd9b-720">fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-720">fieldName</span></span>  

<!-- -->

<span data-ttu-id="edd9b-721">occurence</span><span class="sxs-lookup"><span data-stu-id="edd9b-721">occurence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-722">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-722">arrayIndex</span></span>  

### <a name="method-clearorderby"></a><span data-ttu-id="edd9b-723">メソッド clearOrderBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-723">Method clearOrderBy</span></span>

    public void clearOrderBy()

### <a name="method-clearallfields"></a><span data-ttu-id="edd9b-724">メソッド clearAllFields</span><span class="sxs-lookup"><span data-stu-id="edd9b-724">Method clearAllFields</span></span>

    public void clearAllFields()

### <a name="method-cleargroupby"></a><span data-ttu-id="edd9b-725">メソッド clearGroupBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-725">Method clearGroupBy</span></span>

    public void clearGroupBy()

### <a name="method-autoauthzmode"></a><span data-ttu-id="edd9b-726">メソッド autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="edd9b-726">Method autoAuthzMode</span></span>

    public void autoAuthzMode(AutoAuthzMode mode)

#### <a name="parameters"></a><span data-ttu-id="edd9b-727">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-727">Parameters</span></span>

<span data-ttu-id="edd9b-728">モード</span><span class="sxs-lookup"><span data-stu-id="edd9b-728">mode</span></span>  

### <a name="method-insert_recordset"></a><span data-ttu-id="edd9b-729">メソッド insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="edd9b-729">Method insert\_recordset</span></span>

    public static void insert_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)

#### <a name="parameters"></a><span data-ttu-id="edd9b-730">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-730">Parameters</span></span>

<span data-ttu-id="edd9b-731">targetCursor</span><span class="sxs-lookup"><span data-stu-id="edd9b-731">targetCursor</span></span>  

<!-- -->

<span data-ttu-id="edd9b-732">targetToSourceMap</span><span class="sxs-lookup"><span data-stu-id="edd9b-732">targetToSourceMap</span></span>  

<!-- -->

<span data-ttu-id="edd9b-733">sourceQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-733">sourceQuery</span></span>  

### <a name="method-generatecursors"></a><span data-ttu-id="edd9b-734">メソッド generateCursors</span><span class="sxs-lookup"><span data-stu-id="edd9b-734">Method generateCursors</span></span>

    public void generateCursors()

### <a name="method-checkauthorizationonopenranges"></a><span data-ttu-id="edd9b-735">メソッド checkAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="edd9b-735">Method checkAuthorizationOnOpenRanges</span></span>

    public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)

#### <a name="parameters"></a><span data-ttu-id="edd9b-736">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-736">Parameters</span></span>

<span data-ttu-id="edd9b-737">setCheckAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="edd9b-737">setCheckAuthorizationOnOpenRanges</span></span>  

### <a name="method-addcontains"></a><span data-ttu-id="edd9b-738">メソッド addContains</span><span class="sxs-lookup"><span data-stu-id="edd9b-738">Method addContains</span></span>

    public void addContains(str containsValue, [boolean prefixSearch])

#### <a name="parameters"></a><span data-ttu-id="edd9b-739">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-739">Parameters</span></span>

<span data-ttu-id="edd9b-740">containsValue</span><span class="sxs-lookup"><span data-stu-id="edd9b-740">containsValue</span></span>  

<!-- -->

<span data-ttu-id="edd9b-741">prefixSearch</span><span class="sxs-lookup"><span data-stu-id="edd9b-741">prefixSearch</span></span>  

### <a name="method-resetvalidtimestatequerytype"></a><span data-ttu-id="edd9b-742">メソッド resetValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="edd9b-742">Method resetValidTimeStateQueryType</span></span>

    public void resetValidTimeStateQueryType()

### <a name="method-validtimestatedatetimerange"></a><span data-ttu-id="edd9b-743">メソッド validTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-743">Method validTimeStateDateTimeRange</span></span>

    public void validTimeStateDateTimeRange([DateTime fromDateTime], [DateTime toDateTime])

#### <a name="parameters"></a><span data-ttu-id="edd9b-744">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-744">Parameters</span></span>

<span data-ttu-id="edd9b-745">fromDateTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-745">fromDateTime</span></span>  

<!-- -->

<span data-ttu-id="edd9b-746">toDateTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-746">toDateTime</span></span>  

## <a name="class-querybuilddatasource"></a><span data-ttu-id="edd9b-747">クラス QueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-747">Class QueryBuildDataSource</span></span>
    class QueryBuildDataSource extends TreeNode

<span data-ttu-id="edd9b-748">QueryBuildDataSource クラスは、クエリが構成されているレポート パーツを提供します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-748">The QueryBuildDataSource class provides the building blocks that queries are made of.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-749">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-749">Remarks</span></span>

<span data-ttu-id="edd9b-750">データ ソースは、データ ソースに割り当てられたテーブルからレコードがフェッチされる順序を定義する階層内で配置されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-750">Data sources are arranged in hierarchies that define the sequence in which records are fetched from the tables that are assigned to the data sources.</span></span> <span data-ttu-id="edd9b-751">各データ ソースでは、レコードがフェッチされる順序および選択されたレコードによって満たされなければならない基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-751">Each data source defines the order in which the records are fetched, and also the criteria that must be met by the selected records.</span></span> <span data-ttu-id="edd9b-752">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-752">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="edd9b-753">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-753">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-754">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-754">Examples</span></span>

    {    QueryBuildDataSource ds;    Query q = new Query();        ds = q.addDataSource(        TableNum(CustTable));}

### <a name="methods"></a><span data-ttu-id="edd9b-755">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-755">Methods</span></span>

| <span data-ttu-id="edd9b-756">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-756">Method</span></span>                                                                                                                                                       | <span data-ttu-id="edd9b-757">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-757">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-758">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-758">public int addAllFields(TableName tableName)</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-759">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-759">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span></span>                                                             | <span data-ttu-id="edd9b-760">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-760">Adds a data source that is embedded in this data source.</span></span>                                                                                  |
| <span data-ttu-id="edd9b-761">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-761">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span></span>      |                                                                                                                                           |
| <span data-ttu-id="edd9b-762">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-762">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-763">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-763">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-764">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-764">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-765">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-765">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-766">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-766">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-767">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-767">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-768">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-768">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span></span>                                                             | <span data-ttu-id="edd9b-769">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-769">Adds a range to the data source.</span></span>                                                                                                          |
| <span data-ttu-id="edd9b-770">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-770">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-771">public int addSortIndex(IndexId index)</span><span class="sxs-lookup"><span data-stu-id="edd9b-771">public int addSortIndex(IndexId index)</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-772">public int allowAdd(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-772">public int allowAdd(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-773">public boolean applyFilter(FilterValue filterValue)</span><span class="sxs-lookup"><span data-stu-id="edd9b-773">public boolean applyFilter(FilterValue filterValue)</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-774">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-774">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-775">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-775">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-776">public boolean autoSum(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-776">public boolean autoSum(FieldId field, \[boolean orderNo\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-777">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-777">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-778">public boolean changedNo()</span><span class="sxs-lookup"><span data-stu-id="edd9b-778">public boolean changedNo()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-779">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-779">public int childDataSourceCount()</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-780">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-780">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-781">public str company(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-781">public str company(\[str value\])</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-782">public int concurrencyModel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-782">public int concurrencyModel(\[int value\])</span></span>                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-783">public QueryBuildDynalink dynalink(int dynalinkNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-783">public QueryBuildDynalink dynalink(int dynalinkNo)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-784">public int dynalinkCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-784">public int dynalinkCount()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-785">public boolean embedded()</span><span class="sxs-lookup"><span data-stu-id="edd9b-785">public boolean embedded()</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-786">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-786">public boolean enabled(\[boolean value\])</span></span>                                                                                                                    | <span data-ttu-id="edd9b-787">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-787">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="edd9b-788">public boolean existsMeanOrExists(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-788">public boolean existsMeanOrExists(\[boolean value\])</span></span>                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-789">public int fetchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-789">public int fetchMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-790">public QueryBuildFieldList fields()</span><span class="sxs-lookup"><span data-stu-id="edd9b-790">public QueryBuildFieldList fields()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-791">public TableId file()</span><span class="sxs-lookup"><span data-stu-id="edd9b-791">public TableId file()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-792">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-792">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-793">public boolean firstFast(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-793">public boolean firstFast(\[boolean value\])</span></span>                                                                                                                  | <span data-ttu-id="edd9b-794">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-794">Determines whether to retrieve the first record from the query before the other records.</span></span>                                                  |
| <span data-ttu-id="edd9b-795">public boolean firstOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-795">public boolean firstOnly(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-796">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-796">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-797">public Common getNo()</span><span class="sxs-lookup"><span data-stu-id="edd9b-797">public Common getNo()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-798">public int id()</span><span class="sxs-lookup"><span data-stu-id="edd9b-798">public int id()</span></span>                                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-799">public boolean indexIsHint(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="edd9b-799">public boolean indexIsHint(boolean arg)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-800">public boolean isPartOfSubQueryInBaseQuery()</span><span class="sxs-lookup"><span data-stu-id="edd9b-800">public boolean isPartOfSubQueryInBaseQuery()</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-801">public boolean joined()</span><span class="sxs-lookup"><span data-stu-id="edd9b-801">public boolean joined()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-802">public container joinedDataSources()</span><span class="sxs-lookup"><span data-stu-id="edd9b-802">public container joinedDataSources()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-803">public int joinMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-803">public int joinMode(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-804">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-804">public str label(\[str value\])</span></span>                                                                                                                              | <span data-ttu-id="edd9b-805">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-805">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="edd9b-806">public int level()</span><span class="sxs-lookup"><span data-stu-id="edd9b-806">public int level()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-807">public QueryBuildLink link(int associationNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-807">public QueryBuildLink link(int associationNo)</span></span>                                                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-808">public int linkCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-808">public int linkCount()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-809">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-809">public str name(\[str value\])</span></span>                                                                                                                               | <span data-ttu-id="edd9b-810">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-810">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="edd9b-811">public container oneToOneDataSources()</span><span class="sxs-lookup"><span data-stu-id="edd9b-811">public container oneToOneDataSources()</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-812">public int orderMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-812">public int orderMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-813">public QueryBuildDataSource parentDataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-813">public QueryBuildDataSource parentDataSource()</span></span>                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-814">public str policyContext(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-814">public str policyContext(\[str value\])</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-815">public QueryBuildRange range(int rangeNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-815">public QueryBuildRange range(int rangeNo)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-816">public int rangeCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-816">public int rangeCount()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-817">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-817">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-818">public boolean relations(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-818">public boolean relations(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-819">public int selectionCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-819">public int selectionCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-820">public boolean selectWithRepeatableRead(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-820">public boolean selectWithRepeatableRead(\[boolean value\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-821">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-821">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-822">public FieldId sortField(FieldId field)</span><span class="sxs-lookup"><span data-stu-id="edd9b-822">public FieldId sortField(FieldId field)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-823">public int sortFieldCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-823">public int sortFieldCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-824">public IndexId sortIndex(int indexNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-824">public IndexId sortIndex(int indexNo)</span></span>                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-825">public int sortIndexCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-825">public int sortIndexCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-826">public QueryBuildStaticlink staticlink(int staticlinkNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-826">public QueryBuildStaticlink staticlink(int staticlinkNo)</span></span>                                                                                                     | <span data-ttu-id="edd9b-827">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-827">Returns a static Link object on the query’s data source.</span></span>                                                                                  |
| <span data-ttu-id="edd9b-828">public int staticlinkCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-828">public int staticlinkCount()</span></span>                                                                                                                                 | <span data-ttu-id="edd9b-829">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-829">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>                                                     |
| <span data-ttu-id="edd9b-830">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-830">public TableId table(\[TableId value\])</span></span>                                                                                                                      | <span data-ttu-id="edd9b-831">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-831">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="edd9b-832">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-832">public str toString()</span></span>                                                                                                                                        | <span data-ttu-id="edd9b-833">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-833">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-834">public int unionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-834">public int unionType(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-835">public int uniqueId()</span><span class="sxs-lookup"><span data-stu-id="edd9b-835">public int uniqueId()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-836">public boolean update(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-836">public boolean update(\[boolean value\])</span></span>                                                                                                                     | <span data-ttu-id="edd9b-837">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-837">Determines whether the records fetched by this data source can be updated.</span></span>                                                                |
| <span data-ttu-id="edd9b-838">public void clearLinks()</span><span class="sxs-lookup"><span data-stu-id="edd9b-838">public void clearLinks()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-839">public void clearDynalinks()</span><span class="sxs-lookup"><span data-stu-id="edd9b-839">public void clearDynalinks()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-840">public void clearRange(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-840">public void clearRange(FieldId field, \[int occurrence\])</span></span>                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-841">public void sortClear()</span><span class="sxs-lookup"><span data-stu-id="edd9b-841">public void sortClear()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-842">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-842">public void finalize()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-843">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-843">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-844">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span><span class="sxs-lookup"><span data-stu-id="edd9b-844">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-845">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span><span class="sxs-lookup"><span data-stu-id="edd9b-845">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-846">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-846">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-847">public void clearSortIndex()</span><span class="sxs-lookup"><span data-stu-id="edd9b-847">public void clearSortIndex()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-848">public void clearRanges()</span><span class="sxs-lookup"><span data-stu-id="edd9b-848">public void clearRanges()</span></span>                                                                                                                                    | <span data-ttu-id="edd9b-849">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-849">Deletes all ranges that are associated with the data source.</span></span>                                                                              |
| <span data-ttu-id="edd9b-850">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-850">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-851">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-851">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span></span>                                                               |                                                                                                                                           |

### <a name="method-addallfields"></a><span data-ttu-id="edd9b-852">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="edd9b-852">Method addAllFields</span></span>

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-853">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-853">Parameters</span></span>

<span data-ttu-id="edd9b-854">tableName</span><span class="sxs-lookup"><span data-stu-id="edd9b-854">tableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-855">Return Value</span></span>

### <a name="method-adddatasource"></a><span data-ttu-id="edd9b-856">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-856">Method addDataSource</span></span>

<span data-ttu-id="edd9b-857">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-857">Adds a data source that is embedded in this data source.</span></span>

    public QueryBuildDataSource addDataSource(AnyType arg, [str name], [boolean emptyFieldList])

#### <a name="parameters"></a><span data-ttu-id="edd9b-858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-858">Parameters</span></span>

<span data-ttu-id="edd9b-859">arg</span><span class="sxs-lookup"><span data-stu-id="edd9b-859">arg</span></span>  

<!-- -->

<span data-ttu-id="edd9b-860">名前</span><span class="sxs-lookup"><span data-stu-id="edd9b-860">name</span></span>  

<!-- -->

<span data-ttu-id="edd9b-861">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="edd9b-861">emptyFieldList</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-862">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-862">Return Value</span></span>

<span data-ttu-id="edd9b-863">新しいデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-863">The new data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-864">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-864">Remarks</span></span>

<span data-ttu-id="edd9b-865">最上位レベルのデータ ソースは、addDataSource メソッドを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-865">Top-level data sources are created by using the addDataSource method.</span></span>

### <a name="method-adddynalink"></a><span data-ttu-id="edd9b-866">メソッド addDynalink</span><span class="sxs-lookup"><span data-stu-id="edd9b-866">Method addDynalink</span></span>

    public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, [int fieldArrayIndex], [int dynamicFieldArrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-867">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-867">Parameters</span></span>

<span data-ttu-id="edd9b-868">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-868">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-869">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="edd9b-869">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="edd9b-870">dynamicField</span><span class="sxs-lookup"><span data-stu-id="edd9b-870">dynamicField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-871">fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-871">fieldArrayIndex</span></span>  

<!-- -->

<span data-ttu-id="edd9b-872">dynamicFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-872">dynamicFieldArrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-873">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-873">Return Value</span></span>

### <a name="method-addforeignkeyrelation"></a><span data-ttu-id="edd9b-874">メソッド addForeignkeyRelation</span><span class="sxs-lookup"><span data-stu-id="edd9b-874">Method addForeignkeyRelation</span></span>

    public QueryBuildLink addForeignkeyRelation(str relatedTableRole, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="edd9b-875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-875">Parameters</span></span>

<span data-ttu-id="edd9b-876">relatedTableRole</span><span class="sxs-lookup"><span data-stu-id="edd9b-876">relatedTableRole</span></span>  

<!-- -->

<span data-ttu-id="edd9b-877">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="edd9b-877">parentDatasourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-878">Return Value</span></span>

### <a name="method-addgroupbyfield"></a><span data-ttu-id="edd9b-879">メソッド addGroupByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-879">Method addGroupByField</span></span>

    public QueryGroupByField addGroupByField(FieldId fieldID, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-880">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-880">Parameters</span></span>

<span data-ttu-id="edd9b-881">fieldID</span><span class="sxs-lookup"><span data-stu-id="edd9b-881">fieldID</span></span>  

<!-- -->

<span data-ttu-id="edd9b-882">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-882">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-883">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-883">Return Value</span></span>

### <a name="method-addlink"></a><span data-ttu-id="edd9b-884">メソッド addLink</span><span class="sxs-lookup"><span data-stu-id="edd9b-884">Method addLink</span></span>

    public QueryBuildLink addLink(FieldId parentField, FieldId thisField, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="edd9b-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-885">Parameters</span></span>

<span data-ttu-id="edd9b-886">parentField</span><span class="sxs-lookup"><span data-stu-id="edd9b-886">parentField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-887">thisField</span><span class="sxs-lookup"><span data-stu-id="edd9b-887">thisField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-888">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="edd9b-888">parentDatasourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-889">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-889">Return Value</span></span>

### <a name="method-addorderbyaggregatefield"></a><span data-ttu-id="edd9b-890">メソッド addOrderByAggregateField</span><span class="sxs-lookup"><span data-stu-id="edd9b-890">Method addOrderByAggregateField</span></span>

    public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-891">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-891">Parameters</span></span>

<span data-ttu-id="edd9b-892">fieldType</span><span class="sxs-lookup"><span data-stu-id="edd9b-892">fieldType</span></span>  

<!-- -->

<span data-ttu-id="edd9b-893">fieldID</span><span class="sxs-lookup"><span data-stu-id="edd9b-893">fieldID</span></span>  

<!-- -->

<span data-ttu-id="edd9b-894">direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-894">direction</span></span>  

<!-- -->

<span data-ttu-id="edd9b-895">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-895">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-896">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-896">Return Value</span></span>

### <a name="method-addorderbycalculationfield"></a><span data-ttu-id="edd9b-897">メソッド addOrderByCalculationField</span><span class="sxs-lookup"><span data-stu-id="edd9b-897">Method addOrderByCalculationField</span></span>

    public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, [SortOrder direction])

#### <a name="parameters"></a><span data-ttu-id="edd9b-898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-898">Parameters</span></span>

<span data-ttu-id="edd9b-899">計算</span><span class="sxs-lookup"><span data-stu-id="edd9b-899">calculation</span></span>  

<!-- -->

<span data-ttu-id="edd9b-900">direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-900">direction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-901">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-901">Return Value</span></span>

### <a name="method-addorderbyfield"></a><span data-ttu-id="edd9b-902">メソッド addOrderByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-902">Method addOrderByField</span></span>

    public QueryOrderByField addOrderByField(FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-903">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-903">Parameters</span></span>

<span data-ttu-id="edd9b-904">fieldID</span><span class="sxs-lookup"><span data-stu-id="edd9b-904">fieldID</span></span>  

<!-- -->

<span data-ttu-id="edd9b-905">direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-905">direction</span></span>  

<!-- -->

<span data-ttu-id="edd9b-906">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-906">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-907">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-907">Return Value</span></span>

### <a name="method-addrange"></a><span data-ttu-id="edd9b-908">メソッド addRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-908">Method addRange</span></span>

<span data-ttu-id="edd9b-909">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-909">Adds a range to the data source.</span></span>

    public QueryBuildRange addRange(FieldId field, [int arrayIndex], [QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="edd9b-910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-910">Parameters</span></span>

<span data-ttu-id="edd9b-911">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-911">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-912">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-912">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="edd9b-913">rangeType</span><span class="sxs-lookup"><span data-stu-id="edd9b-913">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-914">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-914">Return Value</span></span>

<span data-ttu-id="edd9b-915">データ ソースの新しい範囲。</span><span class="sxs-lookup"><span data-stu-id="edd9b-915">A new range for the data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-916">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-916">Remarks</span></span>

<span data-ttu-id="edd9b-917">範囲は、データ ソースのテーブルのレコードが満たす必要がある値を定義します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-917">Ranges define the values that records from the data source's table must satisfy.</span></span> <span data-ttu-id="edd9b-918">いくつかの値の範囲は、特定のデータ ソース内の同じフィールドに存在することができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-918">Several range values can exist for the same field in a particular data source.</span></span> <span data-ttu-id="edd9b-919">この場合、レコードが提供される値のいずれかにが適用される場合、値はクエリに含まれます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-919">In this case, the values are included in the query if the record qualifies for any of the values that are supplied.</span></span> <span data-ttu-id="edd9b-920">複数のフィールドの範囲が含まれているときは、両方の条件によって提供される制約を満たすレコードだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-920">When ranges are included for multiple fields, only records that satisfy the constraints that are supplied by both criteria are included.</span></span> <span data-ttu-id="edd9b-921">制約は値のメソッドで指定されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-921">The constraints are specified in the value method.</span></span>

### <a name="method-addsortfield"></a><span data-ttu-id="edd9b-922">メソッド addSortField</span><span class="sxs-lookup"><span data-stu-id="edd9b-922">Method addSortField</span></span>

    public int addSortField(FieldId sortField, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-923">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-923">Parameters</span></span>

<span data-ttu-id="edd9b-924">sortField</span><span class="sxs-lookup"><span data-stu-id="edd9b-924">sortField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-925">direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-925">direction</span></span>  

<!-- -->

<span data-ttu-id="edd9b-926">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-926">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-927">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-927">Return Value</span></span>

### <a name="method-addsortindex"></a><span data-ttu-id="edd9b-928">メソッド addSortIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-928">Method addSortIndex</span></span>

    public int addSortIndex(IndexId index)

#### <a name="parameters"></a><span data-ttu-id="edd9b-929">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-929">Parameters</span></span>

<span data-ttu-id="edd9b-930">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-930">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-931">Return Value</span></span>

### <a name="method-allowadd"></a><span data-ttu-id="edd9b-932">メソッド allowAdd</span><span class="sxs-lookup"><span data-stu-id="edd9b-932">Method allowAdd</span></span>

    public int allowAdd([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-933">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-933">Parameters</span></span>

<span data-ttu-id="edd9b-934">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-934">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-935">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-935">Return Value</span></span>

### <a name="method-applyfilter"></a><span data-ttu-id="edd9b-936">メソッド applyFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-936">Method applyFilter</span></span>

    public boolean applyFilter(FilterValue filterValue)

#### <a name="parameters"></a><span data-ttu-id="edd9b-937">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-937">Parameters</span></span>

<span data-ttu-id="edd9b-938">filterValue</span><span class="sxs-lookup"><span data-stu-id="edd9b-938">filterValue</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-939">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-939">Return Value</span></span>

### <a name="method-autoheader"></a><span data-ttu-id="edd9b-940">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="edd9b-940">Method autoHeader</span></span>

    public boolean autoHeader(FieldId field, [boolean orderNo])

#### <a name="parameters"></a><span data-ttu-id="edd9b-941">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-941">Parameters</span></span>

<span data-ttu-id="edd9b-942">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-942">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-943">orderNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-943">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-944">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-944">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="edd9b-945">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-945">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a><span data-ttu-id="edd9b-946">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-946">Parameters</span></span>

<span data-ttu-id="edd9b-947">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-947">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-948">orderNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-948">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-949">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-949">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="edd9b-950">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="edd9b-950">Method autoSum</span></span>

    public boolean autoSum(FieldId field, [boolean orderNo])

#### <a name="parameters"></a><span data-ttu-id="edd9b-951">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-951">Parameters</span></span>

<span data-ttu-id="edd9b-952">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-952">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-953">orderNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-953">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-954">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-954">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="edd9b-955">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-955">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a><span data-ttu-id="edd9b-956">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-956">Parameters</span></span>

<span data-ttu-id="edd9b-957">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-957">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-958">orderNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-958">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-959">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-959">Return Value</span></span>

### <a name="method-changedno"></a><span data-ttu-id="edd9b-960">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-960">Method changedNo</span></span>

    public boolean changedNo()

#### <a name="return-value"></a><span data-ttu-id="edd9b-961">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-961">Return Value</span></span>

### <a name="method-childdatasourcecount"></a><span data-ttu-id="edd9b-962">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-962">Method childDataSourceCount</span></span>

    public int childDataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-963">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-963">Return Value</span></span>

### <a name="method-childdatasourceno"></a><span data-ttu-id="edd9b-964">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-964">Method childDataSourceNo</span></span>

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-965">Parameters</span></span>

<span data-ttu-id="edd9b-966">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-966">dataSourceNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-967">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-967">Return Value</span></span>

### <a name="method-company"></a><span data-ttu-id="edd9b-968">メソッド company</span><span class="sxs-lookup"><span data-stu-id="edd9b-968">Method company</span></span>

    public str company([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-969">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-969">Parameters</span></span>

<span data-ttu-id="edd9b-970">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-970">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-971">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-971">Return Value</span></span>

### <a name="method-concurrencymodel"></a><span data-ttu-id="edd9b-972">メソッド concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="edd9b-972">Method concurrencyModel</span></span>

    public int concurrencyModel([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-973">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-973">Parameters</span></span>

<span data-ttu-id="edd9b-974">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-974">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-975">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-975">Return Value</span></span>

### <a name="method-dynalink"></a><span data-ttu-id="edd9b-976">メソッド dynalink</span><span class="sxs-lookup"><span data-stu-id="edd9b-976">Method dynalink</span></span>

    public QueryBuildDynalink dynalink(int dynalinkNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-977">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-977">Parameters</span></span>

<span data-ttu-id="edd9b-978">dynalinkNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-978">dynalinkNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-979">Return Value</span></span>

### <a name="method-dynalinkcount"></a><span data-ttu-id="edd9b-980">メソッド dynalinkCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-980">Method dynalinkCount</span></span>

    public int dynalinkCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-981">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-981">Return Value</span></span>

### <a name="method-embedded"></a><span data-ttu-id="edd9b-982">メソッド embedded</span><span class="sxs-lookup"><span data-stu-id="edd9b-982">Method embedded</span></span>

    public boolean embedded()

#### <a name="return-value"></a><span data-ttu-id="edd9b-983">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-983">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="edd9b-984">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="edd9b-984">Method enabled</span></span>

<span data-ttu-id="edd9b-985">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-985">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-986">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-986">Parameters</span></span>

<span data-ttu-id="edd9b-987">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-987">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-988">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-988">Return Value</span></span>

<span data-ttu-id="edd9b-989">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-989">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-990">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-990">Remarks</span></span>

<span data-ttu-id="edd9b-991">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-991">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="edd9b-992">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-992">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="edd9b-993">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-993">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-existsmeanorexists"></a><span data-ttu-id="edd9b-994">メソッド existsMeanOrExists</span><span class="sxs-lookup"><span data-stu-id="edd9b-994">Method existsMeanOrExists</span></span>

    public boolean existsMeanOrExists([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-995">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-995">Parameters</span></span>

<span data-ttu-id="edd9b-996">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-996">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-997">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-997">Return Value</span></span>

### <a name="method-fetchmode"></a><span data-ttu-id="edd9b-998">メソッド fetchMode</span><span class="sxs-lookup"><span data-stu-id="edd9b-998">Method fetchMode</span></span>

    public int fetchMode([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-999">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-999">Parameters</span></span>

<span data-ttu-id="edd9b-1000">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1000">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1001">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1001">Return Value</span></span>

### <a name="method-fields"></a><span data-ttu-id="edd9b-1002">メソッド fields</span><span class="sxs-lookup"><span data-stu-id="edd9b-1002">Method fields</span></span>

    public QueryBuildFieldList fields()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1003">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1003">Return Value</span></span>

### <a name="method-file"></a><span data-ttu-id="edd9b-1004">メソッド file</span><span class="sxs-lookup"><span data-stu-id="edd9b-1004">Method file</span></span>

    public TableId file()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1005">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1005">Return Value</span></span>

### <a name="method-findrange"></a><span data-ttu-id="edd9b-1006">メソッド findRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-1006">Method findRange</span></span>

    public QueryBuildRange findRange(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1007">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1007">Parameters</span></span>

<span data-ttu-id="edd9b-1008">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1008">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1009">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1009">occurrence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1010">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1010">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1011">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1011">Return Value</span></span>

### <a name="method-firstfast"></a><span data-ttu-id="edd9b-1012">メソッド firstFast</span><span class="sxs-lookup"><span data-stu-id="edd9b-1012">Method firstFast</span></span>

<span data-ttu-id="edd9b-1013">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1013">Determines whether to retrieve the first record from the query before the other records.</span></span>

    public boolean firstFast([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1014">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1014">Parameters</span></span>

<span data-ttu-id="edd9b-1015">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1015">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1016">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1016">Return Value</span></span>

<span data-ttu-id="edd9b-1017">最初のレコードが最初に取得される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1017">true if the first record is retrieved first; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1018">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1018">Remarks</span></span>

<span data-ttu-id="edd9b-1019">firstFast プロパティは、一部のデータベース システムでレコードの取得を最適化できるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1019">The firstFast property enables some database systems to optimize record retrieval, which improves performance.</span></span> <span data-ttu-id="edd9b-1020">データベースはこのプロパティをサポートしていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1020">If the database does not support this property, it is ignored.</span></span>

### <a name="method-firstonly"></a><span data-ttu-id="edd9b-1021">メソッド firstOnly</span><span class="sxs-lookup"><span data-stu-id="edd9b-1021">Method firstOnly</span></span>

    public boolean firstOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1022">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1022">Parameters</span></span>

<span data-ttu-id="edd9b-1023">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1023">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1024">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1024">Return Value</span></span>

### <a name="method-getmostrestrictedquerybuildrangestatus"></a><span data-ttu-id="edd9b-1025">メソッド getMostRestrictedQueryBuildRangeStatus</span><span class="sxs-lookup"><span data-stu-id="edd9b-1025">Method getMostRestrictedQueryBuildRangeStatus</span></span>

    public int getMostRestrictedQueryBuildRangeStatus(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1026">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1026">Parameters</span></span>

<span data-ttu-id="edd9b-1027">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1027">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1028">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1028">occurrence</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1029">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1029">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1030">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1030">Return Value</span></span>

### <a name="method-getno"></a><span data-ttu-id="edd9b-1031">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1031">Method getNo</span></span>

    public Common getNo()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1032">Return Value</span></span>

### <a name="method-id"></a><span data-ttu-id="edd9b-1033">メソッド id</span><span class="sxs-lookup"><span data-stu-id="edd9b-1033">Method id</span></span>

    public int id()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1034">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1034">Return Value</span></span>

### <a name="method-indexishint"></a><span data-ttu-id="edd9b-1035">メソッド indexIsHint</span><span class="sxs-lookup"><span data-stu-id="edd9b-1035">Method indexIsHint</span></span>

    public boolean indexIsHint(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1036">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1036">Parameters</span></span>

<span data-ttu-id="edd9b-1037">arg</span><span class="sxs-lookup"><span data-stu-id="edd9b-1037">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1038">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1038">Return Value</span></span>

### <a name="method-ispartofsubqueryinbasequery"></a><span data-ttu-id="edd9b-1039">メソッド isPartOfSubQueryInBaseQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-1039">Method isPartOfSubQueryInBaseQuery</span></span>

    public boolean isPartOfSubQueryInBaseQuery()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1040">Return Value</span></span>

### <a name="method-joined"></a><span data-ttu-id="edd9b-1041">メソッド joined</span><span class="sxs-lookup"><span data-stu-id="edd9b-1041">Method joined</span></span>

    public boolean joined()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1042">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1042">Return Value</span></span>

### <a name="method-joineddatasources"></a><span data-ttu-id="edd9b-1043">メソッド joinedDataSources</span><span class="sxs-lookup"><span data-stu-id="edd9b-1043">Method joinedDataSources</span></span>

    public container joinedDataSources()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1044">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1044">Return Value</span></span>

### <a name="method-joinmode"></a><span data-ttu-id="edd9b-1045">メソッド joinMode</span><span class="sxs-lookup"><span data-stu-id="edd9b-1045">Method joinMode</span></span>

    public int joinMode([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1046">Parameters</span></span>

<span data-ttu-id="edd9b-1047">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1047">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1048">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1048">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="edd9b-1049">メソッド label</span><span class="sxs-lookup"><span data-stu-id="edd9b-1049">Method label</span></span>

<span data-ttu-id="edd9b-1050">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1050">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1051">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1051">Parameters</span></span>

<span data-ttu-id="edd9b-1052">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1052">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1053">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1053">Return Value</span></span>

<span data-ttu-id="edd9b-1054">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1054">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1055">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1055">Remarks</span></span>

<span data-ttu-id="edd9b-1056">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1056">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="edd9b-1057">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1057">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-level"></a><span data-ttu-id="edd9b-1058">メソッド level</span><span class="sxs-lookup"><span data-stu-id="edd9b-1058">Method level</span></span>

    public int level()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1059">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1059">Return Value</span></span>

### <a name="method-link"></a><span data-ttu-id="edd9b-1060">メソッド link</span><span class="sxs-lookup"><span data-stu-id="edd9b-1060">Method link</span></span>

    public QueryBuildLink link(int associationNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1061">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1061">Parameters</span></span>

<span data-ttu-id="edd9b-1062">associationNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1062">associationNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1063">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1063">Return Value</span></span>

### <a name="method-linkcount"></a><span data-ttu-id="edd9b-1064">メソッド linkCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1064">Method linkCount</span></span>

    public int linkCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1065">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1065">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="edd9b-1066">メソッド名</span><span class="sxs-lookup"><span data-stu-id="edd9b-1066">Method name</span></span>

<span data-ttu-id="edd9b-1067">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1067">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1068">Parameters</span></span>

<span data-ttu-id="edd9b-1069">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1069">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1070">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1070">Return Value</span></span>

<span data-ttu-id="edd9b-1071">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1071">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1072">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1072">Remarks</span></span>

<span data-ttu-id="edd9b-1073">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1073">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="edd9b-1074">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1074">Begins with a letter.</span></span>
-   <span data-ttu-id="edd9b-1075">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1075">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="edd9b-1076">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1076">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="edd9b-1077">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1077">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="edd9b-1078">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1078">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-onetoonedatasources"></a><span data-ttu-id="edd9b-1079">メソッド oneToOneDataSources</span><span class="sxs-lookup"><span data-stu-id="edd9b-1079">Method oneToOneDataSources</span></span>

    public container oneToOneDataSources()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1080">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1080">Return Value</span></span>

### <a name="method-ordermode"></a><span data-ttu-id="edd9b-1081">メソッド orderMode</span><span class="sxs-lookup"><span data-stu-id="edd9b-1081">Method orderMode</span></span>

    public int orderMode([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1082">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1082">Parameters</span></span>

<span data-ttu-id="edd9b-1083">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1083">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1084">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1084">Return Value</span></span>

### <a name="method-parentdatasource"></a><span data-ttu-id="edd9b-1085">メソッド parentDataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1085">Method parentDataSource</span></span>

    public QueryBuildDataSource parentDataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1086">Return Value</span></span>

### <a name="method-policycontext"></a><span data-ttu-id="edd9b-1087">メソッド policyContext</span><span class="sxs-lookup"><span data-stu-id="edd9b-1087">Method policyContext</span></span>

    public str policyContext([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1088">Parameters</span></span>

<span data-ttu-id="edd9b-1089">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1089">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1090">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1090">Return Value</span></span>

### <a name="method-range"></a><span data-ttu-id="edd9b-1091">メソッド range</span><span class="sxs-lookup"><span data-stu-id="edd9b-1091">Method range</span></span>

    public QueryBuildRange range(int rangeNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1092">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1092">Parameters</span></span>

<span data-ttu-id="edd9b-1093">rangeNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1093">rangeNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1094">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1094">Return Value</span></span>

### <a name="method-rangecount"></a><span data-ttu-id="edd9b-1095">メソッド rangeCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1095">Method rangeCount</span></span>

    public int rangeCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1096">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1096">Return Value</span></span>

### <a name="method-rangefield"></a><span data-ttu-id="edd9b-1097">メソッド rangeField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1097">Method rangeField</span></span>

    public QueryBuildRange rangeField(FieldId field, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1098">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1098">Parameters</span></span>

<span data-ttu-id="edd9b-1099">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1099">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1100">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1100">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1101">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1101">Return Value</span></span>

### <a name="method-relations"></a><span data-ttu-id="edd9b-1102">メソッド relations</span><span class="sxs-lookup"><span data-stu-id="edd9b-1102">Method relations</span></span>

    public boolean relations([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1103">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1103">Parameters</span></span>

<span data-ttu-id="edd9b-1104">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1104">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1105">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1105">Return Value</span></span>

### <a name="method-selectioncount"></a><span data-ttu-id="edd9b-1106">メソッド selectionCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1106">Method selectionCount</span></span>

    public int selectionCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1107">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1107">Return Value</span></span>

### <a name="method-selectwithrepeatableread"></a><span data-ttu-id="edd9b-1108">メソッド selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="edd9b-1108">Method selectWithRepeatableRead</span></span>

    public boolean selectWithRepeatableRead([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1109">Parameters</span></span>

<span data-ttu-id="edd9b-1110">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1110">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1111">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1111">Return Value</span></span>

### <a name="method-sortdirection"></a><span data-ttu-id="edd9b-1112">メソッド sortDirection</span><span class="sxs-lookup"><span data-stu-id="edd9b-1112">Method sortDirection</span></span>

    public SortOrder sortDirection(FieldId field, [SortOrder direction])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1113">Parameters</span></span>

<span data-ttu-id="edd9b-1114">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1114">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1115">direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-1115">direction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1116">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1116">Return Value</span></span>

### <a name="method-sortfield"></a><span data-ttu-id="edd9b-1117">メソッド sortField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1117">Method sortField</span></span>

    public FieldId sortField(FieldId field)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1118">Parameters</span></span>

<span data-ttu-id="edd9b-1119">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1119">field</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1120">Return Value</span></span>

### <a name="method-sortfieldcount"></a><span data-ttu-id="edd9b-1121">メソッド sortFieldCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1121">Method sortFieldCount</span></span>

    public int sortFieldCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1122">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1122">Return Value</span></span>

### <a name="method-sortindex"></a><span data-ttu-id="edd9b-1123">メソッド sortIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1123">Method sortIndex</span></span>

    public IndexId sortIndex(int indexNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1124">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1124">Parameters</span></span>

<span data-ttu-id="edd9b-1125">indexNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1125">indexNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1126">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1126">Return Value</span></span>

### <a name="method-sortindexcount"></a><span data-ttu-id="edd9b-1127">メソッド sortIndexCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1127">Method sortIndexCount</span></span>

    public int sortIndexCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1128">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1128">Return Value</span></span>

### <a name="method-staticlink"></a><span data-ttu-id="edd9b-1129">メソッド staticlink</span><span class="sxs-lookup"><span data-stu-id="edd9b-1129">Method staticlink</span></span>

<span data-ttu-id="edd9b-1130">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1130">Returns a static Link object on the query’s data source.</span></span>

    public QueryBuildStaticlink staticlink(int staticlinkNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1131">Parameters</span></span>

<span data-ttu-id="edd9b-1132">staticlinkNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1132">staticlinkNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1133">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1133">Return Value</span></span>

<span data-ttu-id="edd9b-1134">\_staticLinkNo インデックスの静的リンク オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1134">The static Link object at the \_staticLinkNo index.</span></span>

### <a name="method-staticlinkcount"></a><span data-ttu-id="edd9b-1135">メソッド staticlinkCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1135">Method staticlinkCount</span></span>

<span data-ttu-id="edd9b-1136">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1136">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>

    public int staticlinkCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1137">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1137">Return Value</span></span>

<span data-ttu-id="edd9b-1138">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1138">The number of static links that are defined on the QueryBuildDataSource object.</span></span>

### <a name="method-table"></a><span data-ttu-id="edd9b-1139">メソッド table</span><span class="sxs-lookup"><span data-stu-id="edd9b-1139">Method table</span></span>

<span data-ttu-id="edd9b-1140">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1140">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1141">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1141">Parameters</span></span>

<span data-ttu-id="edd9b-1142">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1142">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1143">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1143">Return Value</span></span>

<span data-ttu-id="edd9b-1144">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1144">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-1145">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-1145">Method toString</span></span>

<span data-ttu-id="edd9b-1146">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1146">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1147">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1147">Return Value</span></span>

<span data-ttu-id="edd9b-1148">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1148">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1149">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1149">Remarks</span></span>

<span data-ttu-id="edd9b-1150">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1150">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-1151">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1151">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-1152">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1152">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-uniontype"></a><span data-ttu-id="edd9b-1153">メソッド unionType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1153">Method unionType</span></span>

    public int unionType([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1154">Parameters</span></span>

<span data-ttu-id="edd9b-1155">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1155">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1156">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1156">Return Value</span></span>

### <a name="method-uniqueid"></a><span data-ttu-id="edd9b-1157">メソッド uniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-1157">Method uniqueId</span></span>

    public int uniqueId()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1158">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1158">Return Value</span></span>

### <a name="method-update"></a><span data-ttu-id="edd9b-1159">メソッド update</span><span class="sxs-lookup"><span data-stu-id="edd9b-1159">Method update</span></span>

<span data-ttu-id="edd9b-1160">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1160">Determines whether the records fetched by this data source can be updated.</span></span>

    public boolean update([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1161">Parameters</span></span>

<span data-ttu-id="edd9b-1162">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1162">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1163">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1163">Return Value</span></span>

<span data-ttu-id="edd9b-1164">レコードを更新することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1164">true if the records can be updated; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1165">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1165">Remarks</span></span>

<span data-ttu-id="edd9b-1166">レコードを更新するには、ttsBegin および ttsCommit メソッドを使用して別のトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1166">To update the records, start a separate transaction by using the ttsBegin and ttsCommit methods.</span></span>

### <a name="method-clearlinks"></a><span data-ttu-id="edd9b-1167">メソッド clearLinks</span><span class="sxs-lookup"><span data-stu-id="edd9b-1167">Method clearLinks</span></span>

    public void clearLinks()

### <a name="method-cleardynalinks"></a><span data-ttu-id="edd9b-1168">メソッド clearDynalinks</span><span class="sxs-lookup"><span data-stu-id="edd9b-1168">Method clearDynalinks</span></span>

    public void clearDynalinks()

### <a name="method-clearrange"></a><span data-ttu-id="edd9b-1169">メソッド clearRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-1169">Method clearRange</span></span>

    public void clearRange(FieldId field, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1170">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1170">Parameters</span></span>

<span data-ttu-id="edd9b-1171">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1171">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1172">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1172">occurrence</span></span>  

### <a name="method-sortclear"></a><span data-ttu-id="edd9b-1173">メソッド sortClear</span><span class="sxs-lookup"><span data-stu-id="edd9b-1173">Method sortClear</span></span>

    public void sortClear()

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1174">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1174">Method finalize</span></span>

    public void finalize()

### <a name="method-addselectionfieldwithalias"></a><span data-ttu-id="edd9b-1175">メソッド addSelectionFieldWithAlias</span><span class="sxs-lookup"><span data-stu-id="edd9b-1175">Method addSelectionFieldWithAlias</span></span>

    public void addSelectionFieldWithAlias(str alias, FieldId field, [SelectionField fieldType])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1176">Parameters</span></span>

<span data-ttu-id="edd9b-1177">エイリアス</span><span class="sxs-lookup"><span data-stu-id="edd9b-1177">alias</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1178">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1178">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1179">fieldType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1179">fieldType</span></span>  

### <a name="method-addcalculationfield"></a><span data-ttu-id="edd9b-1180">メソッド addCalculationField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1180">Method addCalculationField</span></span>

    public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1181">Parameters</span></span>

<span data-ttu-id="edd9b-1182">計算</span><span class="sxs-lookup"><span data-stu-id="edd9b-1182">calculation</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1183">エイリアス</span><span class="sxs-lookup"><span data-stu-id="edd9b-1183">alias</span></span>  

### <a name="method-addforeignkeydynalink"></a><span data-ttu-id="edd9b-1184">メソッド addForeignKeyDynalink</span><span class="sxs-lookup"><span data-stu-id="edd9b-1184">Method addForeignKeyDynalink</span></span>

    public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1185">Parameters</span></span>

<span data-ttu-id="edd9b-1186">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="edd9b-1186">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1187">relatedRole</span><span class="sxs-lookup"><span data-stu-id="edd9b-1187">relatedRole</span></span>  

### <a name="method-addrelation"></a><span data-ttu-id="edd9b-1188">メソッド addRelation</span><span class="sxs-lookup"><span data-stu-id="edd9b-1188">Method addRelation</span></span>

    public void addRelation(DictRelation relation, [TableScope tableScope])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1189">Parameters</span></span>

<span data-ttu-id="edd9b-1190">関係</span><span class="sxs-lookup"><span data-stu-id="edd9b-1190">relation</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1191">tableScope</span><span class="sxs-lookup"><span data-stu-id="edd9b-1191">tableScope</span></span>  

### <a name="method-clearsortindex"></a><span data-ttu-id="edd9b-1192">メソッド clearSortIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1192">Method clearSortIndex</span></span>

    public void clearSortIndex()

### <a name="method-clearranges"></a><span data-ttu-id="edd9b-1193">メソッド clearRanges</span><span class="sxs-lookup"><span data-stu-id="edd9b-1193">Method clearRanges</span></span>

<span data-ttu-id="edd9b-1194">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1194">Deletes all ranges that are associated with the data source.</span></span>

    public void clearRanges()

#### <a name="examples"></a><span data-ttu-id="edd9b-1195">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1195">Examples</span></span>

<span data-ttu-id="edd9b-1196">次の例では、範囲を追加し、データソースから範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1196">The following example adds ranges and then removes them from a data source.</span></span>

    Query Q = new Query(); 
    QueryBuildDataSource ds = q.addDataSource(TableNum(CustTable)); 
    QueryBuildRange r = ds.addRange(FieldNum(CustTable, recId)); 
    print ds.rangeCount(); 
    ds.clearRanges(); 
    print ds.rangeCount(); 
    pause;

### <a name="method-linkfields"></a><span data-ttu-id="edd9b-1197">メソッド linkFields</span><span class="sxs-lookup"><span data-stu-id="edd9b-1197">Method linkFields</span></span>

    public void linkFields(str parentField, str thisField, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1198">Parameters</span></span>

<span data-ttu-id="edd9b-1199">parentField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1199">parentField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1200">thisField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1200">thisField</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1201">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1201">parentDatasourceName</span></span>  

### <a name="method-addselectionfield"></a><span data-ttu-id="edd9b-1202">メソッド addSelectionField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1202">Method addSelectionField</span></span>

    public void addSelectionField(FieldId field, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1203">Parameters</span></span>

<span data-ttu-id="edd9b-1204">フィールド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1204">field</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1205">fieldType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1205">fieldType</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1206">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1206">arrayIndex</span></span>  

## <a name="class-querybuilddynalink"></a><span data-ttu-id="edd9b-1207">クラス QueryBuildDynalink</span><span class="sxs-lookup"><span data-stu-id="edd9b-1207">Class QueryBuildDynalink</span></span>
    class QueryBuildDynalink extends Object

### <a name="remarks"></a><span data-ttu-id="edd9b-1208">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1208">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1209">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1209">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1210">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1210">Methods</span></span>

| <span data-ttu-id="edd9b-1211">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1211">Method</span></span>                                                | <span data-ttu-id="edd9b-1212">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1212">Description</span></span> |
|-------------------------------------------------------|-------------|
| <span data-ttu-id="edd9b-1213">public Common cursor(\[Common cursor\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1213">public Common cursor(\[Common cursor\])</span></span>               |             |
| <span data-ttu-id="edd9b-1214">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1214">public QueryBuildDataSource dataSource()</span></span>              |             |
| <span data-ttu-id="edd9b-1215">public FieldId dynamicField(\[FieldId dynamicField\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1215">public FieldId dynamicField(\[FieldId dynamicField\])</span></span> |             |
| <span data-ttu-id="edd9b-1216">public FieldId field(\[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1216">public FieldId field(\[FieldId fieldId\])</span></span>             |             |
| <span data-ttu-id="edd9b-1217">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1217">public int fieldArrayIndex()</span></span>                          |             |
| <span data-ttu-id="edd9b-1218">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1218">public FieldName fieldName()</span></span>                          |             |
| <span data-ttu-id="edd9b-1219">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1219">public void finalize()</span></span>                                |             |

### <a name="method-cursor"></a><span data-ttu-id="edd9b-1220">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="edd9b-1220">Method cursor</span></span>

    public Common cursor([Common cursor])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1221">Parameters</span></span>

<span data-ttu-id="edd9b-1222">cursor</span><span class="sxs-lookup"><span data-stu-id="edd9b-1222">cursor</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1223">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1223">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1224">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1224">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1225">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1225">Return Value</span></span>

### <a name="method-dynamicfield"></a><span data-ttu-id="edd9b-1226">メソッド dynamicField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1226">Method dynamicField</span></span>

    public FieldId dynamicField([FieldId dynamicField])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1227">Parameters</span></span>

<span data-ttu-id="edd9b-1228">dynamicField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1228">dynamicField</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1229">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1229">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1230">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1230">Method field</span></span>

    public FieldId field([FieldId fieldId])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1231">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1231">Parameters</span></span>

<span data-ttu-id="edd9b-1232">fieldId</span><span class="sxs-lookup"><span data-stu-id="edd9b-1232">fieldId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1233">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1233">Return Value</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="edd9b-1234">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1234">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1235">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="edd9b-1236">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1236">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1237">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1237">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1238">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1238">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildfieldlist"></a><span data-ttu-id="edd9b-1239">クラス QueryBuildFieldList</span><span class="sxs-lookup"><span data-stu-id="edd9b-1239">Class QueryBuildFieldList</span></span>
    class QueryBuildFieldList extends TreeNode

<span data-ttu-id="edd9b-1240">QueryBuildFieldList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1240">The QueryBuildFieldList class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-1241">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1241">Remarks</span></span>

<span data-ttu-id="edd9b-1242">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1242">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1243">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1243">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1244">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1244">Methods</span></span>

| <span data-ttu-id="edd9b-1245">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1245">Method</span></span>                                                                                                 | <span data-ttu-id="edd9b-1246">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1246">Description</span></span> |
|--------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="edd9b-1247">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1247">public int addAllFields(TableName tableName)</span></span>                                                           |             |
| <span data-ttu-id="edd9b-1248">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1248">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span></span> |             |
| <span data-ttu-id="edd9b-1249">public int dynamic(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1249">public int dynamic(\[int value\])</span></span>                                                                      |             |
| <span data-ttu-id="edd9b-1250">public FieldId field(int index)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1250">public FieldId field(int index)</span></span>                                                                        |             |
| <span data-ttu-id="edd9b-1251">public int fieldCount()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1251">public int fieldCount()</span></span>                                                                                |             |
| <span data-ttu-id="edd9b-1252">public SelectionField fieldKind(int index)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1252">public SelectionField fieldKind(int index)</span></span>                                                             |             |
| <span data-ttu-id="edd9b-1253">public TableId tableSelector(int index)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1253">public TableId tableSelector(int index)</span></span>                                                                |             |
| <span data-ttu-id="edd9b-1254">public void clearFieldList()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1254">public void clearFieldList()</span></span>                                                                           |             |

### <a name="method-addallfields"></a><span data-ttu-id="edd9b-1255">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="edd9b-1255">Method addAllFields</span></span>

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1256">Parameters</span></span>

<span data-ttu-id="edd9b-1257">tableName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1257">tableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1258">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1258">Return Value</span></span>

### <a name="method-addfield"></a><span data-ttu-id="edd9b-1259">メソッド addField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1259">Method addField</span></span>

    public QueryBuildFieldList addField(FieldId fieldId, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1260">Parameters</span></span>

<span data-ttu-id="edd9b-1261">fieldId</span><span class="sxs-lookup"><span data-stu-id="edd9b-1261">fieldId</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1262">fieldType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1262">fieldType</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1263">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1263">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1264">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1264">Return Value</span></span>

### <a name="method-dynamic"></a><span data-ttu-id="edd9b-1265">メソッド dynamic</span><span class="sxs-lookup"><span data-stu-id="edd9b-1265">Method dynamic</span></span>

    public int dynamic([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1266">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1266">Parameters</span></span>

<span data-ttu-id="edd9b-1267">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1267">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1268">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1268">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1269">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1269">Method field</span></span>

    public FieldId field(int index)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1270">Parameters</span></span>

<span data-ttu-id="edd9b-1271">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-1271">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1272">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1272">Return Value</span></span>

### <a name="method-fieldcount"></a><span data-ttu-id="edd9b-1273">メソッド fieldCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-1273">Method fieldCount</span></span>

    public int fieldCount()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1274">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1274">Return Value</span></span>

### <a name="method-fieldkind"></a><span data-ttu-id="edd9b-1275">メソッド fieldKind</span><span class="sxs-lookup"><span data-stu-id="edd9b-1275">Method fieldKind</span></span>

    public SelectionField fieldKind(int index)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1276">Parameters</span></span>

<span data-ttu-id="edd9b-1277">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-1277">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1278">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1278">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="edd9b-1279">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1279">Method tableSelector</span></span>

    public TableId tableSelector(int index)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1280">Parameters</span></span>

<span data-ttu-id="edd9b-1281">指数</span><span class="sxs-lookup"><span data-stu-id="edd9b-1281">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1282">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1282">Return Value</span></span>

### <a name="method-clearfieldlist"></a><span data-ttu-id="edd9b-1283">メソッド clearFieldList</span><span class="sxs-lookup"><span data-stu-id="edd9b-1283">Method clearFieldList</span></span>

    public void clearFieldList()

## <a name="class-querybuildlink"></a><span data-ttu-id="edd9b-1284">クラス QueryBuildLink</span><span class="sxs-lookup"><span data-stu-id="edd9b-1284">Class QueryBuildLink</span></span>
    class QueryBuildLink extends TreeNode

<span data-ttu-id="edd9b-1285">QueryBuildLink クラスは、X++ コードおよびメタデータの作成、読み取り、更新、および削除を可能にします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1285">The QueryBuildLink class enables for the creating, reading, updating, and deleting of X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-1286">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1286">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1287">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1287">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1288">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1288">Methods</span></span>

| <span data-ttu-id="edd9b-1289">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1289">Method</span></span>                      | <span data-ttu-id="edd9b-1290">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1290">Description</span></span> |
|-----------------------------|-------------|
| <span data-ttu-id="edd9b-1291">public int delete()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1291">public int delete()</span></span>         |             |
| <span data-ttu-id="edd9b-1292">public int field()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1292">public int field()</span></span>          |             |
| <span data-ttu-id="edd9b-1293">public boolean incomplete()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1293">public boolean incomplete()</span></span> |             |
| <span data-ttu-id="edd9b-1294">public str joinRelation()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1294">public str joinRelation()</span></span>   |             |
| <span data-ttu-id="edd9b-1295">public int relatedField()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1295">public int relatedField()</span></span>   |             |
| <span data-ttu-id="edd9b-1296">public int relatedTable()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1296">public int relatedTable()</span></span>   |             |
| <span data-ttu-id="edd9b-1297">public int table()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1297">public int table()</span></span>          |             |
| <span data-ttu-id="edd9b-1298">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1298">public void finalize()</span></span>      |             |

### <a name="method-delete"></a><span data-ttu-id="edd9b-1299">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="edd9b-1299">Method delete</span></span>

    public int delete()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1300">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1300">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1301">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1301">Method field</span></span>

    public int field()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1302">Return Value</span></span>

### <a name="method-incomplete"></a><span data-ttu-id="edd9b-1303">メソッド incomplete</span><span class="sxs-lookup"><span data-stu-id="edd9b-1303">Method incomplete</span></span>

    public boolean incomplete()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1304">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1304">Return Value</span></span>

### <a name="method-joinrelation"></a><span data-ttu-id="edd9b-1305">メソッド joinRelation</span><span class="sxs-lookup"><span data-stu-id="edd9b-1305">Method joinRelation</span></span>

    public str joinRelation()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1306">Return Value</span></span>

### <a name="method-relatedfield"></a><span data-ttu-id="edd9b-1307">メソッド relatedField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1307">Method relatedField</span></span>

    public int relatedField()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1308">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1308">Return Value</span></span>

### <a name="method-relatedtable"></a><span data-ttu-id="edd9b-1309">メソッド relatedTable</span><span class="sxs-lookup"><span data-stu-id="edd9b-1309">Method relatedTable</span></span>

    public int relatedTable()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1310">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1310">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="edd9b-1311">メソッド table</span><span class="sxs-lookup"><span data-stu-id="edd9b-1311">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1312">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1312">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1313">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1313">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildrange"></a><span data-ttu-id="edd9b-1314">クラス QueryBuildRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-1314">Class QueryBuildRange</span></span>
    class QueryBuildRange extends TreeNode

<span data-ttu-id="edd9b-1315">QueryBuildRange クラスは、QueryBuildRange クラスが関連付けられているデータ ソースからフェッチするレコードを定義する範囲を表します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1315">The QueryBuildRange class represents the ranges that define which records should be fetched from the data source in which the QueryBuildRange class is associated.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-1316">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1316">Remarks</span></span>

<span data-ttu-id="edd9b-1317">value プロパティを使用して、範囲を定義する文字列を設定できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1317">The value property can be used to set the string that defines the range.</span></span> <span data-ttu-id="edd9b-1318">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1318">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="edd9b-1319">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1319">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="edd9b-1320">特定のデータ ソースは、任意の数の範囲を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1320">A particular data source can have any number of ranges.</span></span> <span data-ttu-id="edd9b-1321">複数の範囲は、同じデータ ソース フィールドに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1321">Multiple ranges are valid for the same data source field.</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1322">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1322">Examples</span></span>

<span data-ttu-id="edd9b-1323">次の基本的な例は、QueryBuildRange クラスを使用して特定のデータ フィールドの対象範囲を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1323">The following basic example shows how to use the QueryBuildRange class to specify the range of interest for a specific data field.</span></span>

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

### <a name="methods"></a><span data-ttu-id="edd9b-1324">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1324">Methods</span></span>

| <span data-ttu-id="edd9b-1325">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1325">Method</span></span>                                                        | <span data-ttu-id="edd9b-1326">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1326">Description</span></span>                                                                                                                               |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-1327">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1327">public QueryBuildDataSource dataSource()</span></span>                      | <span data-ttu-id="edd9b-1328">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1328">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>                                                          |
| <span data-ttu-id="edd9b-1329">public boolean doesRangeNodeBelongToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1329">public boolean doesRangeNodeBelongToCompositeQuery()</span></span>          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1330">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1330">public boolean enabled(\[boolean value\])</span></span>                     | <span data-ttu-id="edd9b-1331">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1331">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="edd9b-1332">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1332">public FieldId field(\[FieldId value\])</span></span>                       | <span data-ttu-id="edd9b-1333">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1333">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="edd9b-1334">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1334">public int fieldArrayIndex()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-1335">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1335">public FieldName fieldName()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-1336">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1336">public str label(\[str value\])</span></span>                               | <span data-ttu-id="edd9b-1337">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1337">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="edd9b-1338">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1338">public str name(\[str value\])</span></span>                                | <span data-ttu-id="edd9b-1339">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1339">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="edd9b-1340">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1340">public str prompt()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-1341">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1341">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-1342">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1342">public int status(\[int value\])</span></span>                              | <span data-ttu-id="edd9b-1343">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1343">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="edd9b-1344">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1344">public TableId table(\[TableId value\])</span></span>                       | <span data-ttu-id="edd9b-1345">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1345">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="edd9b-1346">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1346">public TableId tableSelector(\[TableId value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="edd9b-1347">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1347">public str toString()</span></span>                                         | <span data-ttu-id="edd9b-1348">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1348">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-1349">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1349">public int typeof()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-1350">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1350">public boolean valid()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="edd9b-1351">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1351">public str value(\[str value\])</span></span>                               | <span data-ttu-id="edd9b-1352">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1352">Gets or sets the value that queried records must match to be retrieved.</span></span>                                                                   |
| <span data-ttu-id="edd9b-1353">public void associateRangeNodeToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1353">public void associateRangeNodeToCompositeQuery()</span></span>              |                                                                                                                                           |
| <span data-ttu-id="edd9b-1354">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1354">public void finalize()</span></span>                                        |                                                                                                                                           |

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1355">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1355">Method dataSource</span></span>

<span data-ttu-id="edd9b-1356">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1356">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1357">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1357">Return Value</span></span>

<span data-ttu-id="edd9b-1358">QueryBuildRange クラスオブジェクトのインスタンスを作成するために使用されたデータソース。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1358">The data source that was used to instantiate the QueryBuildRange class object.</span></span>

### <a name="method-doesrangenodebelongtocompositequery"></a><span data-ttu-id="edd9b-1359">メソッド doesRangeNodeBelongToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-1359">Method doesRangeNodeBelongToCompositeQuery</span></span>

    public boolean doesRangeNodeBelongToCompositeQuery()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1360">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1360">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="edd9b-1361">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="edd9b-1361">Method enabled</span></span>

<span data-ttu-id="edd9b-1362">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1362">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1363">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1363">Parameters</span></span>

<span data-ttu-id="edd9b-1364">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1364">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1365">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1365">Return Value</span></span>

<span data-ttu-id="edd9b-1366">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1366">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1367">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1367">Remarks</span></span>

<span data-ttu-id="edd9b-1368">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1368">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="edd9b-1369">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1369">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="edd9b-1370">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1370">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1371">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1371">Method field</span></span>

<span data-ttu-id="edd9b-1372">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1372">Gets or sets the field ID associated with the object.</span></span>

    public FieldId field([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1373">Parameters</span></span>

<span data-ttu-id="edd9b-1374">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1374">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1375">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1375">Return Value</span></span>

<span data-ttu-id="edd9b-1376">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1376">The current value of the field ID associated with the object.</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="edd9b-1377">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1377">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1378">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1378">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="edd9b-1379">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1379">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1380">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1380">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="edd9b-1381">メソッド label</span><span class="sxs-lookup"><span data-stu-id="edd9b-1381">Method label</span></span>

<span data-ttu-id="edd9b-1382">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1382">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1383">Parameters</span></span>

<span data-ttu-id="edd9b-1384">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1384">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1385">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1385">Return Value</span></span>

<span data-ttu-id="edd9b-1386">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1386">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1387">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1387">Remarks</span></span>

<span data-ttu-id="edd9b-1388">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1388">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="edd9b-1389">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1389">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="edd9b-1390">メソッド名</span><span class="sxs-lookup"><span data-stu-id="edd9b-1390">Method name</span></span>

<span data-ttu-id="edd9b-1391">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1391">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1392">Parameters</span></span>

<span data-ttu-id="edd9b-1393">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1393">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1394">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1394">Return Value</span></span>

<span data-ttu-id="edd9b-1395">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1395">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1396">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1396">Remarks</span></span>

<span data-ttu-id="edd9b-1397">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1397">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="edd9b-1398">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1398">Begins with a letter.</span></span>
-   <span data-ttu-id="edd9b-1399">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1399">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="edd9b-1400">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1400">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="edd9b-1401">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1401">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="edd9b-1402">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1402">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-prompt"></a><span data-ttu-id="edd9b-1403">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="edd9b-1403">Method prompt</span></span>

    public str prompt()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1404">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1404">Return Value</span></span>

### <a name="method-rangetype"></a><span data-ttu-id="edd9b-1405">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1405">Method rangeType</span></span>

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1406">Parameters</span></span>

<span data-ttu-id="edd9b-1407">rangeType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1407">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1408">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1408">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="edd9b-1409">メソッド status</span><span class="sxs-lookup"><span data-stu-id="edd9b-1409">Method status</span></span>

<span data-ttu-id="edd9b-1410">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1410">Gets or sets the status of an object.</span></span>

    public int status([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1411">Parameters</span></span>

<span data-ttu-id="edd9b-1412">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1412">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1413">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1413">Return Value</span></span>

<span data-ttu-id="edd9b-1414">オブジェクトの現在の状態</span><span class="sxs-lookup"><span data-stu-id="edd9b-1414">The current status of the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1415">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1415">Remarks</span></span>

<span data-ttu-id="edd9b-1416">ステータスには次の値があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1416">The following values are possible for the status:</span></span>

-   <span data-ttu-id="edd9b-1417">0 - ステータス オープン。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1417">0 – Status Open.</span></span>
-   <span data-ttu-id="edd9b-1418">1 - ステータス ロック。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1418">1 – Status Lock.</span></span>
-   <span data-ttu-id="edd9b-1419">2 - ステータスが非表示です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1419">2 – Status Hide.</span></span>

### <a name="method-table"></a><span data-ttu-id="edd9b-1420">メソッド table</span><span class="sxs-lookup"><span data-stu-id="edd9b-1420">Method table</span></span>

<span data-ttu-id="edd9b-1421">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1421">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1422">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1422">Parameters</span></span>

<span data-ttu-id="edd9b-1423">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1423">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1424">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1424">Return Value</span></span>

<span data-ttu-id="edd9b-1425">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1425">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="edd9b-1426">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1426">Method tableSelector</span></span>

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1427">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1427">Parameters</span></span>

<span data-ttu-id="edd9b-1428">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1428">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1429">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1429">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-1430">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-1430">Method toString</span></span>

<span data-ttu-id="edd9b-1431">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1431">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1432">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1432">Return Value</span></span>

<span data-ttu-id="edd9b-1433">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1433">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1434">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1434">Remarks</span></span>

<span data-ttu-id="edd9b-1435">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1435">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-1436">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1436">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-1437">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1437">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-typeof"></a><span data-ttu-id="edd9b-1438">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="edd9b-1438">Method typeof</span></span>

    public int typeof()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1439">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1439">Return Value</span></span>

### <a name="method-valid"></a><span data-ttu-id="edd9b-1440">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="edd9b-1440">Method valid</span></span>

    public boolean valid()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1441">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1441">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="edd9b-1442">メソッド value</span><span class="sxs-lookup"><span data-stu-id="edd9b-1442">Method value</span></span>

<span data-ttu-id="edd9b-1443">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1443">Gets or sets the value that queried records must match to be retrieved.</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1444">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1444">Parameters</span></span>

<span data-ttu-id="edd9b-1445">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1445">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1446">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1446">Return Value</span></span>

<span data-ttu-id="edd9b-1447">範囲の文字列値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1447">The string value for the range.</span></span>

### <a name="method-associaterangenodetocompositequery"></a><span data-ttu-id="edd9b-1448">メソッド associateRangeNodeToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-1448">Method associateRangeNodeToCompositeQuery</span></span>

    public void associateRangeNodeToCompositeQuery()

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1449">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1449">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildstaticlink"></a><span data-ttu-id="edd9b-1450">クラス QueryBuildStaticlink</span><span class="sxs-lookup"><span data-stu-id="edd9b-1450">Class QueryBuildStaticlink</span></span>
    class QueryBuildStaticlink extends Object

<span data-ttu-id="edd9b-1451">QueryBuildStaticLink クラスは、QueryBuildDataSource クラスで定義されている静的リンクに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1451">The QueryBuildStaticLink class provides the information about the static links that are defined on a QueryBuildDataSource class.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-1452">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1452">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1453">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1453">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1454">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1454">Methods</span></span>

| <span data-ttu-id="edd9b-1455">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1455">Method</span></span>                 | <span data-ttu-id="edd9b-1456">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1456">Description</span></span>                                                         |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edd9b-1457">public FieldId field()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1457">public FieldId field()</span></span> | <span data-ttu-id="edd9b-1458">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="edd9b-1458">Provides the field information on which the static link is defined/</span></span> |
| <span data-ttu-id="edd9b-1459">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1459">public AnyType value()</span></span> | <span data-ttu-id="edd9b-1460">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1460">Gets the value of the field on which the static link is defined.</span></span>    |
| <span data-ttu-id="edd9b-1461">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1461">public void finalize()</span></span> |                                                                     |

### <a name="method-field"></a><span data-ttu-id="edd9b-1462">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1462">Method field</span></span>

<span data-ttu-id="edd9b-1463">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="edd9b-1463">Provides the field information on which the static link is defined/</span></span>

    public FieldId field()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1464">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1464">Return Value</span></span>

<span data-ttu-id="edd9b-1465">静的リンクが定義されているフィールドの FieldId 値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1465">The FieldId value of the field on which the static link is defined.</span></span>

### <a name="method-value"></a><span data-ttu-id="edd9b-1466">メソッド value</span><span class="sxs-lookup"><span data-stu-id="edd9b-1466">Method value</span></span>

<span data-ttu-id="edd9b-1467">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1467">Gets the value of the field on which the static link is defined.</span></span>

    public AnyType value()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1468">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1468">Return Value</span></span>

<span data-ttu-id="edd9b-1469">静的リンクの値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1469">The value of the static link.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1470">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1470">Method finalize</span></span>

    public void finalize()

## <a name="class-queryfilter"></a><span data-ttu-id="edd9b-1471">クラス QueryFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-1471">Class QueryFilter</span></span>
    class QueryFilter extends Object

### <a name="remarks"></a><span data-ttu-id="edd9b-1472">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1472">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1473">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1473">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1474">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1474">Methods</span></span>

| <span data-ttu-id="edd9b-1475">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1475">Method</span></span>                                                        | <span data-ttu-id="edd9b-1476">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1476">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="edd9b-1477">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1477">public QueryBuildDataSource dataSource()</span></span>                      |                                                      |
| <span data-ttu-id="edd9b-1478">public FieldName field()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1478">public FieldName field()</span></span>                                      |                                                      |
| <span data-ttu-id="edd9b-1479">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1479">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                      |
| <span data-ttu-id="edd9b-1480">public int status(\[int status\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1480">public int status(\[int status\])</span></span>                             |                                                      |
| <span data-ttu-id="edd9b-1481">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1481">public str toString()</span></span>                                         | <span data-ttu-id="edd9b-1482">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1482">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="edd9b-1483">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1483">public str value(\[str value\])</span></span>                               |                                                      |
| <span data-ttu-id="edd9b-1484">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1484">public void finalize()</span></span>                                        |                                                      |

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1485">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1485">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1486">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1486">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1487">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1487">Method field</span></span>

    public FieldName field()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1488">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1488">Return Value</span></span>

### <a name="method-rangetype"></a><span data-ttu-id="edd9b-1489">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1489">Method rangeType</span></span>

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1490">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1490">Parameters</span></span>

<span data-ttu-id="edd9b-1491">rangeType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1491">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1492">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1492">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="edd9b-1493">メソッド status</span><span class="sxs-lookup"><span data-stu-id="edd9b-1493">Method status</span></span>

    public int status([int status])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1494">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1494">Parameters</span></span>

<span data-ttu-id="edd9b-1495">ステータス</span><span class="sxs-lookup"><span data-stu-id="edd9b-1495">status</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1496">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1496">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-1497">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-1497">Method toString</span></span>

<span data-ttu-id="edd9b-1498">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1498">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1499">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1499">Return Value</span></span>

<span data-ttu-id="edd9b-1500">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1500">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1501">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1501">Remarks</span></span>

<span data-ttu-id="edd9b-1502">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1502">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-1503">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1503">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-1504">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1504">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="edd9b-1505">メソッド value</span><span class="sxs-lookup"><span data-stu-id="edd9b-1505">Method value</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1506">Parameters</span></span>

<span data-ttu-id="edd9b-1507">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1507">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1508">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1508">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1509">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1509">Method finalize</span></span>

    public void finalize()

## <a name="class-querygroupbyfield"></a><span data-ttu-id="edd9b-1510">クラス QueryGroupByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1510">Class QueryGroupByField</span></span>
    class QueryGroupByField extends TreeNode

### <a name="remarks"></a><span data-ttu-id="edd9b-1511">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1511">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1512">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1512">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1513">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1513">Methods</span></span>

| <span data-ttu-id="edd9b-1514">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1514">Method</span></span>                                                  | <span data-ttu-id="edd9b-1515">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1515">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="edd9b-1516">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1516">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="edd9b-1517">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1517">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="edd9b-1518">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1518">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="edd9b-1519">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1519">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="edd9b-1520">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1520">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="edd9b-1521">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1521">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="edd9b-1522">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1522">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="edd9b-1523">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1523">public void finalize()</span></span>                                  |             |

### <a name="method-autoheader"></a><span data-ttu-id="edd9b-1524">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="edd9b-1524">Method autoHeader</span></span>

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1525">Parameters</span></span>

<span data-ttu-id="edd9b-1526">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1526">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1527">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="edd9b-1528">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-1528">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1529">Parameters</span></span>

<span data-ttu-id="edd9b-1530">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1530">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1531">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1531">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="edd9b-1532">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="edd9b-1532">Method autoSum</span></span>

    public boolean autoSum([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1533">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1533">Parameters</span></span>

<span data-ttu-id="edd9b-1534">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1534">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1535">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1535">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="edd9b-1536">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-1536">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1537">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1537">Parameters</span></span>

<span data-ttu-id="edd9b-1538">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1538">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1539">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1539">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1540">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1540">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1541">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1541">Return Value</span></span>

### <a name="method-fieldid"></a><span data-ttu-id="edd9b-1542">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="edd9b-1542">Method fieldID</span></span>

    public int fieldID()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1543">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1543">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="edd9b-1544">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1544">Method tableSelector</span></span>

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1545">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1545">Parameters</span></span>

<span data-ttu-id="edd9b-1546">tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1546">tableSelector</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1547">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1547">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1548">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1548">Method finalize</span></span>

    public void finalize()

## <a name="class-queryhavingfilter"></a><span data-ttu-id="edd9b-1549">クラス QueryHavingFilter</span><span class="sxs-lookup"><span data-stu-id="edd9b-1549">Class QueryHavingFilter</span></span>
    class QueryHavingFilter extends TreeNode

### <a name="remarks"></a><span data-ttu-id="edd9b-1550">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1550">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1551">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1551">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1552">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1552">Methods</span></span>

| <span data-ttu-id="edd9b-1553">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1553">Method</span></span>                                          | <span data-ttu-id="edd9b-1554">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1554">Description</span></span>                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-1555">public AggregateFunction aggregateFunction()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1555">public AggregateFunction aggregateFunction()</span></span>    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1556">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1556">public QueryBuildDataSource dataSource()</span></span>        |                                                                                                                                           |
| <span data-ttu-id="edd9b-1557">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1557">public boolean enabled(\[boolean value\])</span></span>       | <span data-ttu-id="edd9b-1558">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1558">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="edd9b-1559">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1559">public FieldId field(\[FieldId value\])</span></span>         | <span data-ttu-id="edd9b-1560">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1560">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="edd9b-1561">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1561">public int fieldArrayIndex()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1562">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1562">public FieldName fieldName()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1563">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1563">public str label(\[str value\])</span></span>                 | <span data-ttu-id="edd9b-1564">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1564">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="edd9b-1565">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1565">public str name(\[str value\])</span></span>                  | <span data-ttu-id="edd9b-1566">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1566">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="edd9b-1567">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1567">public str prompt()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-1568">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1568">public int status(\[int value\])</span></span>                | <span data-ttu-id="edd9b-1569">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1569">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="edd9b-1570">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1570">public TableId table(\[TableId value\])</span></span>         | <span data-ttu-id="edd9b-1571">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1571">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="edd9b-1572">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1572">public TableId tableSelector(\[TableId value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-1573">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1573">public str toString()</span></span>                           | <span data-ttu-id="edd9b-1574">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1574">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-1575">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1575">public int typeof()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-1576">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1576">public boolean valid()</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1577">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1577">public str value(\[str value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-1578">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1578">public void finalize()</span></span>                          |                                                                                                                                           |

### <a name="method-aggregatefunction"></a><span data-ttu-id="edd9b-1579">メソッド aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="edd9b-1579">Method aggregateFunction</span></span>

    public AggregateFunction aggregateFunction()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1580">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1580">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1581">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1581">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1582">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1582">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="edd9b-1583">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="edd9b-1583">Method enabled</span></span>

<span data-ttu-id="edd9b-1584">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1584">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1585">Parameters</span></span>

<span data-ttu-id="edd9b-1586">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1586">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1587">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1587">Return Value</span></span>

<span data-ttu-id="edd9b-1588">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1588">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1589">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1589">Remarks</span></span>

<span data-ttu-id="edd9b-1590">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1590">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="edd9b-1591">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1591">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="edd9b-1592">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1592">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-field"></a><span data-ttu-id="edd9b-1593">メソッド field</span><span class="sxs-lookup"><span data-stu-id="edd9b-1593">Method field</span></span>

<span data-ttu-id="edd9b-1594">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1594">Gets or sets the field ID associated with the object.</span></span>

    public FieldId field([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1595">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1595">Parameters</span></span>

<span data-ttu-id="edd9b-1596">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1596">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1597">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1597">Return Value</span></span>

<span data-ttu-id="edd9b-1598">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1598">The current value of the field ID associated with the object.</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="edd9b-1599">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="edd9b-1599">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1600">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1600">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="edd9b-1601">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1601">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1602">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1602">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="edd9b-1603">メソッド label</span><span class="sxs-lookup"><span data-stu-id="edd9b-1603">Method label</span></span>

<span data-ttu-id="edd9b-1604">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1604">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1605">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1605">Parameters</span></span>

<span data-ttu-id="edd9b-1606">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1606">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1607">Return Value</span></span>

<span data-ttu-id="edd9b-1608">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1608">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1609">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1609">Remarks</span></span>

<span data-ttu-id="edd9b-1610">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1610">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="edd9b-1611">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1611">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="edd9b-1612">メソッド名</span><span class="sxs-lookup"><span data-stu-id="edd9b-1612">Method name</span></span>

<span data-ttu-id="edd9b-1613">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1613">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1614">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1614">Parameters</span></span>

<span data-ttu-id="edd9b-1615">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1615">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1616">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1616">Return Value</span></span>

<span data-ttu-id="edd9b-1617">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1617">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1618">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1618">Remarks</span></span>

<span data-ttu-id="edd9b-1619">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1619">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="edd9b-1620">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1620">Begins with a letter.</span></span>
-   <span data-ttu-id="edd9b-1621">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1621">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="edd9b-1622">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1622">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="edd9b-1623">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1623">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="edd9b-1624">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1624">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-prompt"></a><span data-ttu-id="edd9b-1625">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="edd9b-1625">Method prompt</span></span>

    public str prompt()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1626">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1626">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="edd9b-1627">メソッド status</span><span class="sxs-lookup"><span data-stu-id="edd9b-1627">Method status</span></span>

<span data-ttu-id="edd9b-1628">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1628">Gets or sets the status of an object.</span></span>

    public int status([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1629">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1629">Parameters</span></span>

<span data-ttu-id="edd9b-1630">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1630">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1631">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1631">Return Value</span></span>

<span data-ttu-id="edd9b-1632">オブジェクトのステータスの現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1632">The current value of the status of the object.</span></span>

### <a name="method-table"></a><span data-ttu-id="edd9b-1633">メソッド table</span><span class="sxs-lookup"><span data-stu-id="edd9b-1633">Method table</span></span>

<span data-ttu-id="edd9b-1634">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1634">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1635">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1635">Parameters</span></span>

<span data-ttu-id="edd9b-1636">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1636">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1637">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1637">Return Value</span></span>

<span data-ttu-id="edd9b-1638">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1638">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="edd9b-1639">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1639">Method tableSelector</span></span>

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1640">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1640">Parameters</span></span>

<span data-ttu-id="edd9b-1641">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1641">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1642">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1642">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-1643">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-1643">Method toString</span></span>

<span data-ttu-id="edd9b-1644">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1644">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1645">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1645">Return Value</span></span>

<span data-ttu-id="edd9b-1646">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1646">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1647">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1647">Remarks</span></span>

<span data-ttu-id="edd9b-1648">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1648">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-1649">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1649">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-1650">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1650">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-typeof"></a><span data-ttu-id="edd9b-1651">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="edd9b-1651">Method typeof</span></span>

    public int typeof()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1652">Return Value</span></span>

### <a name="method-valid"></a><span data-ttu-id="edd9b-1653">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="edd9b-1653">Method valid</span></span>

    public boolean valid()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1654">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1654">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="edd9b-1655">メソッド value</span><span class="sxs-lookup"><span data-stu-id="edd9b-1655">Method value</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1656">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1656">Parameters</span></span>

<span data-ttu-id="edd9b-1657">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1657">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1658">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1658">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1659">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1659">Method finalize</span></span>

    public void finalize()

## <a name="class-queryorderbyfield"></a><span data-ttu-id="edd9b-1660">クラス QueryOrderByField</span><span class="sxs-lookup"><span data-stu-id="edd9b-1660">Class QueryOrderByField</span></span>
    class QueryOrderByField extends TreeNode

### <a name="remarks"></a><span data-ttu-id="edd9b-1661">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1661">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1662">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1662">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="edd9b-1663">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1663">Methods</span></span>

| <span data-ttu-id="edd9b-1664">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1664">Method</span></span>                                                  | <span data-ttu-id="edd9b-1665">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1665">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="edd9b-1666">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1666">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="edd9b-1667">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1667">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="edd9b-1668">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1668">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="edd9b-1669">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1669">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="edd9b-1670">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1670">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="edd9b-1671">public SortOrder direction()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1671">public SortOrder direction()</span></span>                            |             |
| <span data-ttu-id="edd9b-1672">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1672">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="edd9b-1673">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1673">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="edd9b-1674">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1674">public void finalize()</span></span>                                  |             |

### <a name="method-autoheader"></a><span data-ttu-id="edd9b-1675">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="edd9b-1675">Method autoHeader</span></span>

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1676">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1676">Parameters</span></span>

<span data-ttu-id="edd9b-1677">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1677">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1678">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1678">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="edd9b-1679">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-1679">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1680">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1680">Parameters</span></span>

<span data-ttu-id="edd9b-1681">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1681">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1682">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1682">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="edd9b-1683">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="edd9b-1683">Method autoSum</span></span>

    public boolean autoSum([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1684">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1684">Parameters</span></span>

<span data-ttu-id="edd9b-1685">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1685">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1686">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1686">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="edd9b-1687">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="edd9b-1687">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1688">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1688">Parameters</span></span>

<span data-ttu-id="edd9b-1689">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1689">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1690">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1690">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="edd9b-1691">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="edd9b-1691">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1692">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1692">Return Value</span></span>

### <a name="method-direction"></a><span data-ttu-id="edd9b-1693">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="edd9b-1693">Method direction</span></span>

    public SortOrder direction()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1694">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1694">Return Value</span></span>

### <a name="method-fieldid"></a><span data-ttu-id="edd9b-1695">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="edd9b-1695">Method fieldID</span></span>

    public int fieldID()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1696">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1696">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="edd9b-1697">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1697">Method tableSelector</span></span>

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1698">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1698">Parameters</span></span>

<span data-ttu-id="edd9b-1699">tableSelector</span><span class="sxs-lookup"><span data-stu-id="edd9b-1699">tableSelector</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1700">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1700">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="edd9b-1701">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="edd9b-1701">Method finalize</span></span>

    public void finalize()

## <a name="class-queryrun"></a><span data-ttu-id="edd9b-1702">クラス QueryRun</span><span class="sxs-lookup"><span data-stu-id="edd9b-1702">Class QueryRun</span></span>
    class QueryRun extends ObjectRun

<span data-ttu-id="edd9b-1703">QueryRun クラスは、データベース内のテーブルをスキャンし、ユーザーによって与えられている制約を満たすレコードをフェッチして、ユーザー入力からこのような制約を収集するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1703">The QueryRun class traverses tables in the database, fetches records that satisfy constraints that are given by the user, and helps to gather such constraints from user input.</span></span>

### <a name="remarks"></a><span data-ttu-id="edd9b-1704">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1704">Remarks</span></span>

<span data-ttu-id="edd9b-1705">QueryRun オブジェクトは、データベース内のテーブルをスキャンし、ユーザーが指定した制約を満たすレコードをフェッチするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1705">QueryRun objects are used to traverse tables in the database and fetch records that satisfy the constraints that are given by the user.</span></span> <span data-ttu-id="edd9b-1706">QueryRun オブジェクトは、ユーザーがそのような制限を入力できるように、ユーザーと通信することができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1706">A QueryRun object may interact with the user to let the user enter such constraints.</span></span> <span data-ttu-id="edd9b-1707">クエリは、レポートに表示するデータを記述してフェッチするためにレポートにより内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1707">Queries are used internally by reports to delineate and fetch the data to be presented in the report.</span></span> <span data-ttu-id="edd9b-1708">QueryRun オブジェクトは、クエリ オブジェクト を使用してクエリの構造を定義します (たとえば、どのテーブルを検索するか、レコードをどのように並び替えるかなど)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1708">A QueryRun object relies on a Query object to define the structure of the query (for example, which tables are searched and how the records are sorted).</span></span> <span data-ttu-id="edd9b-1709">QueryRun オブジェクトは、クエリの動的動作を定義しますが、クエリ オブジェクトはクエリの静的特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1709">A QueryRun object defines the dynamic behavior of the query, whereas a Query object defines the static characteristics of the query.</span></span>

### <a name="examples"></a><span data-ttu-id="edd9b-1710">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1710">Examples</span></span>

<span data-ttu-id="edd9b-1711">次の例では、アプリケーション オブジェクト ツリー (AOT) での顧客という名前のクエリがあり、そこに 1 つのデータ ソース CustTable テーブルがあると見なされます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1711">In the following example, it is assumed that there is a query named Customer in the Application Object Tree (AOT), and that it has one data source, the CustTable table.</span></span>

    static void example() 
    { 
        // Create a QueryRun object from a query stored in the AOT. 
        QueryRun qr = new QueryRun ("Customer"); 
        CustTable customerRecord; 
        // Display a window enabling the user to choose which records to print. 
        if (qr.prompt()) 
        { 
            // The user clicked OK. 
            while (qr.next()) 
            { 
                // Get the fetched record. 
                CustomerRecord = qr.GetNo(1); 
                // Do something with it 
                print CustomerRecord.AccountNum; 
            } 
        } 
        else 
        { 
            // The user pressed Cancel, so do nothing. 
        } 
    }

### <a name="methods"></a><span data-ttu-id="edd9b-1712">メソッド</span><span class="sxs-lookup"><span data-stu-id="edd9b-1712">Methods</span></span>

| <span data-ttu-id="edd9b-1713">方法</span><span class="sxs-lookup"><span data-stu-id="edd9b-1713">Method</span></span>                                                                                                         | <span data-ttu-id="edd9b-1714">説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1714">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd9b-1715">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1715">public boolean allowCheck(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-1716">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1716">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-1717">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1717">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-1718">public boolean changed(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1718">public boolean changed(TableId table, \[int occurrence\])</span></span>                                                      | <span data-ttu-id="edd9b-1719">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1719">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>                     |
| <span data-ttu-id="edd9b-1720">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1720">public str changedBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="edd9b-1721">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1721">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="edd9b-1722">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1722">public Date changedDate(\[Date value\])</span></span>                                                                        | <span data-ttu-id="edd9b-1723">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1723">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="edd9b-1724">public boolean changedNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1724">public boolean changedNo(int dataSourceNo)</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-1725">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1725">public str changedTime(\[str value\])</span></span>                                                                          | <span data-ttu-id="edd9b-1726">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1726">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="edd9b-1727">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1727">public str createdBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="edd9b-1728">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1728">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="edd9b-1729">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1729">public Date creationDate(\[Date value\])</span></span>                                                                       | <span data-ttu-id="edd9b-1730">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1730">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="edd9b-1731">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1731">public str creationTime(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-1732">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1732">public str description(\[str value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1733">public boolean equal(Object obj)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1733">public boolean equal(Object obj)</span></span>                                                                               | <span data-ttu-id="edd9b-1734">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1734">Determines whether the specified object is equal to the current object.</span></span>                                                                   |
| <span data-ttu-id="edd9b-1735">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1735">public str form(\[str value\])</span></span>                                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-1736">public Common get(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1736">public Common get(TableId table, \[int occurrence\])</span></span>                                                           | <span data-ttu-id="edd9b-1737">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1737">Retrieves the record fetched by the previous call to next method.</span></span>                                                                         |
| <span data-ttu-id="edd9b-1738">public System.Type getImpExpDataContractType()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1738">public System.Type getImpExpDataContractType()</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-1739">public Common getNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1739">public Common getNo(int dataSourceNo)</span></span>                                                                          | <span data-ttu-id="edd9b-1740">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1740">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>                                                                |
| <span data-ttu-id="edd9b-1741">public boolean importable()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1741">public boolean importable()</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1742">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1742">public boolean interactive(\[boolean value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="edd9b-1743">public boolean isPositionPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1743">public boolean isPositionPagingEnabled()</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="edd9b-1744">public boolean isQueryTimedout()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1744">public boolean isQueryTimedout()</span></span>                                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-1745">public boolean isValueBasedPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1745">public boolean isValueBasedPagingEnabled()</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-1746">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1746">public int literals(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-1747">public Guid loadCsv(str fileName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1747">public Guid loadCsv(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-1748">public Guid loadXml(str fileName)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1748">public Guid loadXml(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-1749">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1749">public str name(\[str value\])</span></span>                                                                                 | <span data-ttu-id="edd9b-1750">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1750">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="edd9b-1751">public QueryRun newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1751">public QueryRun newObject(AnyType source)</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-1752">public boolean next()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1752">public boolean next()</span></span>                                                                                          | <span data-ttu-id="edd9b-1753">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1753">Retrieves the next record from the query.</span></span>                                                                                                 |
| <span data-ttu-id="edd9b-1754">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1754">public int nextUniqueId(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-1755">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1755">public Guid origin(\[Guid value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-1756">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1756">public container pack(\[boolean doCheck\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="edd9b-1757">public boolean prompt()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1757">public boolean prompt()</span></span>                                                                                        | <span data-ttu-id="edd9b-1758">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1758">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>                                                   |
| <span data-ttu-id="edd9b-1759">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1759">public Query query(\[Query query\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-1760">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1760">public int queryType(\[int value\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-1761">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1761">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1762">public ReportRun report()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1762">public ReportRun report()</span></span>                                                                                      |                                                                                                                                           |
| <span data-ttu-id="edd9b-1763">public ReportRun reportRun()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1763">public ReportRun reportRun()</span></span>                                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-1764">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1764">public boolean saved()</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-1765">public boolean saveUserSetup(\[boolean saveIt\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1765">public boolean saveUserSetup(\[boolean saveIt\])</span></span>                                                               | <span data-ttu-id="edd9b-1766">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1766">Saves the user setup.</span></span>                                                                                                                     |
| <span data-ttu-id="edd9b-1767">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1767">public boolean searchable(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-1768">public boolean setCursor(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1768">public boolean setCursor(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1769">public boolean setRecord(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1769">public boolean setRecord(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="edd9b-1770">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1770">public str title(\[str value\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="edd9b-1771">public str toString()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1771">public str toString()</span></span>                                                                                          | <span data-ttu-id="edd9b-1772">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1772">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="edd9b-1773">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1773">public boolean userUpdate(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="edd9b-1774">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1774">public int version(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="edd9b-1775">::public static int getQueryRowCount(Query query, int maxRows)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1775">::public static int getQueryRowCount(Query query, int maxRows)</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-1776">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1776">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span></span> |                                                                                                                                           |
| <span data-ttu-id="edd9b-1777">public void run()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1777">public void run()</span></span>                                                                                              | <span data-ttu-id="edd9b-1778">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1778">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>                                  |
| <span data-ttu-id="edd9b-1779">public void new(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1779">public void new(AnyType source)</span></span>                                                                                | <span data-ttu-id="edd9b-1780">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1780">Initializes a new instance of the Object class.</span></span>                                                                                           |
| <span data-ttu-id="edd9b-1781">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1781">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-1782">public void reset()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1782">public void reset()</span></span>                                                                                            |                                                                                                                                           |
| <span data-ttu-id="edd9b-1783">public void setImportSession(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1783">public void setImportSession(Guid importSession)</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="edd9b-1784">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1784">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="edd9b-1785">public void init()</span><span class="sxs-lookup"><span data-stu-id="edd9b-1785">public void init()</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="edd9b-1786">public void enablePositionPaging(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1786">public void enablePositionPaging(\[boolean enabled\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1787">public void shred(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="edd9b-1787">public void shred(Guid importSession)</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="edd9b-1788">public void enableValueBasedPaging(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1788">public void enableValueBasedPaging(\[boolean enable\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="edd9b-1789">public void bulkNext(\[boolean fetchAllData\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1789">public void bulkNext(\[boolean fetchAllData\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="edd9b-1790">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span><span class="sxs-lookup"><span data-stu-id="edd9b-1790">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span></span>                              |                                                                                                                                           |

### <a name="method-allowcheck"></a><span data-ttu-id="edd9b-1791">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="edd9b-1791">Method allowCheck</span></span>

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1792">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1792">Parameters</span></span>

<span data-ttu-id="edd9b-1793">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1793">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1794">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1794">Return Value</span></span>

### <a name="method-allowcrosscompany"></a><span data-ttu-id="edd9b-1795">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="edd9b-1795">Method allowCrossCompany</span></span>

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1796">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1796">Parameters</span></span>

<span data-ttu-id="edd9b-1797">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1797">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1798">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1798">Return Value</span></span>

### <a name="method-canpage"></a><span data-ttu-id="edd9b-1799">メソッド canPage</span><span class="sxs-lookup"><span data-stu-id="edd9b-1799">Method canPage</span></span>

    public boolean canPage([boolean skipOrderByCheck], [boolean throwIfNotPagable], [boolean isValuePaging])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1800">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1800">Parameters</span></span>

<span data-ttu-id="edd9b-1801">skipOrderByCheck</span><span class="sxs-lookup"><span data-stu-id="edd9b-1801">skipOrderByCheck</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1802">throwIfNotPagable</span><span class="sxs-lookup"><span data-stu-id="edd9b-1802">throwIfNotPagable</span></span>  

<!-- -->

<span data-ttu-id="edd9b-1803">isValuePaging</span><span class="sxs-lookup"><span data-stu-id="edd9b-1803">isValuePaging</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1804">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1804">Return Value</span></span>

### <a name="method-changed"></a><span data-ttu-id="edd9b-1805">メソッド changed</span><span class="sxs-lookup"><span data-stu-id="edd9b-1805">Method changed</span></span>

<span data-ttu-id="edd9b-1806">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1806">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>

    public boolean changed(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1807">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1807">Parameters</span></span>

<span data-ttu-id="edd9b-1808">テーブル</span><span class="sxs-lookup"><span data-stu-id="edd9b-1808">table</span></span>  
<span data-ttu-id="edd9b-1809">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1809">The data source to check; optional.</span></span> <span data-ttu-id="edd9b-1810">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1810">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

<!-- -->

<span data-ttu-id="edd9b-1811">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1811">occurrence</span></span>  
<span data-ttu-id="edd9b-1812">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1812">The data source to check; optional.</span></span> <span data-ttu-id="edd9b-1813">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1813">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-1814">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1814">Return Value</span></span>

<span data-ttu-id="edd9b-1815">QueryRun.next に対する最後の呼び出し後に指定データ ソースが変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1815">true if the specified data source has changed since the last call to QueryRun.next; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1816">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1816">Remarks</span></span>

<span data-ttu-id="edd9b-1817">このメソッドは、データ ソースが階層構造になっている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1817">This method is useful when data sources are hierarchically structured.</span></span> <span data-ttu-id="edd9b-1818">埋め込みデータ ソースは、何回でも変更できます (顧客トランザクションなど)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1818">A more embedded data source may change many times (such as the customer transactions).</span></span> <span data-ttu-id="edd9b-1819">これは、埋め込まれていないデータソース (顧客テーブルなど) が新しいレコード (別の顧客) をフェッチするたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1819">This occurs every time that a less embedded data source (such as the customer table) fetches a new record (another customer).</span></span> <span data-ttu-id="edd9b-1820">この関数の代わりに changedNo メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1820">The changedNo method can be used instead of this function.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="edd9b-1821">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-1821">Method changedBy</span></span>

<span data-ttu-id="edd9b-1822">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1822">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1823">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1823">Parameters</span></span>

<span data-ttu-id="edd9b-1824">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1824">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1825">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1825">Return Value</span></span>

<span data-ttu-id="edd9b-1826">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1826">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="edd9b-1827">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-1827">Method changedDate</span></span>

<span data-ttu-id="edd9b-1828">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1828">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1829">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1829">Parameters</span></span>

<span data-ttu-id="edd9b-1830">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1830">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1831">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1831">Return Value</span></span>

<span data-ttu-id="edd9b-1832">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1832">The date an application object was last changed.</span></span>

### <a name="method-changedno"></a><span data-ttu-id="edd9b-1833">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1833">Method changedNo</span></span>

    public boolean changedNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1834">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1834">Parameters</span></span>

<span data-ttu-id="edd9b-1835">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1835">dataSourceNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1836">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1836">Return Value</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="edd9b-1837">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-1837">Method changedTime</span></span>

<span data-ttu-id="edd9b-1838">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1838">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1839">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1839">Parameters</span></span>

<span data-ttu-id="edd9b-1840">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1840">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1841">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1841">Return Value</span></span>

<span data-ttu-id="edd9b-1842">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1842">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="edd9b-1843">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-1843">Method createdBy</span></span>

<span data-ttu-id="edd9b-1844">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1844">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1845">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1845">Parameters</span></span>

<span data-ttu-id="edd9b-1846">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1846">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1847">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1847">Return Value</span></span>

<span data-ttu-id="edd9b-1848">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1848">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="edd9b-1849">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="edd9b-1849">Method creationDate</span></span>

<span data-ttu-id="edd9b-1850">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1850">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1851">Parameters</span></span>

<span data-ttu-id="edd9b-1852">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1852">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1853">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1853">Return Value</span></span>

<span data-ttu-id="edd9b-1854">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1854">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="edd9b-1855">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="edd9b-1855">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1856">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1856">Parameters</span></span>

<span data-ttu-id="edd9b-1857">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1857">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1858">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1858">Return Value</span></span>

### <a name="method-description"></a><span data-ttu-id="edd9b-1859">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="edd9b-1859">Method description</span></span>

    public str description([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1860">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1860">Parameters</span></span>

<span data-ttu-id="edd9b-1861">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1861">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1862">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1862">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="edd9b-1863">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="edd9b-1863">Method equal</span></span>

<span data-ttu-id="edd9b-1864">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1864">Determines whether the specified object is equal to the current object.</span></span>

    public boolean equal(Object obj)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1865">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1865">Parameters</span></span>

<span data-ttu-id="edd9b-1866">obj</span><span class="sxs-lookup"><span data-stu-id="edd9b-1866">obj</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1867">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1867">Return Value</span></span>

<span data-ttu-id="edd9b-1868">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1868">true if the specified object is equal to the current object; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1869">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1869">Remarks</span></span>

<span data-ttu-id="edd9b-1870">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1870">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="edd9b-1871">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1871">However, derived classes can override the Object::equal method to support value equality.</span></span>

### <a name="method-form"></a><span data-ttu-id="edd9b-1872">メソッド form</span><span class="sxs-lookup"><span data-stu-id="edd9b-1872">Method form</span></span>

    public str form([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1873">Parameters</span></span>

<span data-ttu-id="edd9b-1874">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1874">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1875">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1875">Return Value</span></span>

### <a name="method-get"></a><span data-ttu-id="edd9b-1876">メソッド get</span><span class="sxs-lookup"><span data-stu-id="edd9b-1876">Method get</span></span>

<span data-ttu-id="edd9b-1877">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1877">Retrieves the record fetched by the previous call to next method.</span></span>

    public Common get(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1878">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1878">Parameters</span></span>

<span data-ttu-id="edd9b-1879">テーブル</span><span class="sxs-lookup"><span data-stu-id="edd9b-1879">table</span></span>  
<span data-ttu-id="edd9b-1880">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1880">The data source to be addressed; optional.</span></span> <span data-ttu-id="edd9b-1881">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1881">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="edd9b-1882">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1882">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="edd9b-1883">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1883">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="edd9b-1884">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1884">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

<!-- -->

<span data-ttu-id="edd9b-1885">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-1885">occurrence</span></span>  
<span data-ttu-id="edd9b-1886">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1886">The data source to be addressed; optional.</span></span> <span data-ttu-id="edd9b-1887">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1887">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="edd9b-1888">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1888">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="edd9b-1889">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1889">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="edd9b-1890">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1890">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-1891">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1891">Return Value</span></span>

<span data-ttu-id="edd9b-1892">引数で識別されるデータ ソースからフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1892">Returns the record fetched from the data source identified by the arguments.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1893">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1893">Remarks</span></span>

<span data-ttu-id="edd9b-1894">レコードを取得するデータ ソースは、データ ソースに割り当てられたテーブルとオプションのパラメーターによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1894">The data source from which to retrieve the record is specified by the table assigned to the data source and by an optional parameter.</span></span> <span data-ttu-id="edd9b-1895">テーブル (およびオプションのパラメーター) を指定するのではなく、getNo メソッドを使用して、データ ソースの数を引数として取得できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1895">Instead of supplying the table (and optional parameter), you can use the getNo method, which takes the data source number as an argument.</span></span>

### <a name="method-getimpexpdatacontracttype"></a><span data-ttu-id="edd9b-1896">メソッド getImpExpDataContractType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1896">Method getImpExpDataContractType</span></span>

    public System.Type getImpExpDataContractType()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1897">Return Value</span></span>

### <a name="method-getno"></a><span data-ttu-id="edd9b-1898">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1898">Method getNo</span></span>

<span data-ttu-id="edd9b-1899">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1899">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>

    public Common getNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1900">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1900">Parameters</span></span>

<span data-ttu-id="edd9b-1901">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="edd9b-1901">dataSourceNo</span></span>  
<span data-ttu-id="edd9b-1902">現在選択されているレコードを取得する元のデータ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1902">The number of the data source from which to get the currently selected record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="edd9b-1903">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1903">Return Value</span></span>

<span data-ttu-id="edd9b-1904">引数で識別されるデータ ソースのフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1904">Returns the record fetched for the data source identified by the argument.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1905">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1905">Remarks</span></span>

<span data-ttu-id="edd9b-1906">レコードを取り出すデータ ソースは、データ ソースの番号で指定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1906">The data source from which to retrieve the record is specified by the number of the data source.</span></span> <span data-ttu-id="edd9b-1907">データソースは、1 から順にカウントされます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1907">The data sources are counted consecutively, starting from 1.</span></span> <span data-ttu-id="edd9b-1908">代わりに QueryRun.get メソッドを使用できます。このメソッドは、データ ソースを定義するテーブル (およびオプション パラメーター) を使用して指定されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1908">The QueryRun.get Method method can be used instead; that method is supplied with the table (and an optional parameter), that defines the data source.</span></span>

#### <a name="examples"></a><span data-ttu-id="edd9b-1909">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1909">Examples</span></span>

    { 
        QueryRun qr; 
        // Consider a query with CustTable/CustTrans datasources. 
        // Traverse all records found in CustTable/CustTrans: 
        while (qr.next()) 
        { 
            if (qr.Changed(TableNum(CustTable)))
            { 
                // A new CustTable record 
                CustTableRecord = qr.GetNo(1); 
            } 
            if (qr.Changed(TableNum(CustTrans))) 
            { 
                // A new CustTrans record 
                CustTransRecord = qr.GetNo(1); 
            } 
        } 
    }

### <a name="method-importable"></a><span data-ttu-id="edd9b-1910">メソッド importable</span><span class="sxs-lookup"><span data-stu-id="edd9b-1910">Method importable</span></span>

    public boolean importable()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1911">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1911">Return Value</span></span>

### <a name="method-interactive"></a><span data-ttu-id="edd9b-1912">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="edd9b-1912">Method interactive</span></span>

    public boolean interactive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1913">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1913">Parameters</span></span>

<span data-ttu-id="edd9b-1914">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1914">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1915">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1915">Return Value</span></span>

### <a name="method-ispositionpagingenabled"></a><span data-ttu-id="edd9b-1916">メソッド isPositionPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="edd9b-1916">Method isPositionPagingEnabled</span></span>

    public boolean isPositionPagingEnabled()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1917">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1917">Return Value</span></span>

### <a name="method-isquerytimedout"></a><span data-ttu-id="edd9b-1918">メソッド isQueryTimedout</span><span class="sxs-lookup"><span data-stu-id="edd9b-1918">Method isQueryTimedout</span></span>

    public boolean isQueryTimedout()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1919">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1919">Return Value</span></span>

### <a name="method-isvaluebasedpagingenabled"></a><span data-ttu-id="edd9b-1920">メソッド isValueBasedPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="edd9b-1920">Method isValueBasedPagingEnabled</span></span>

    public boolean isValueBasedPagingEnabled()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1921">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1921">Return Value</span></span>

### <a name="method-literals"></a><span data-ttu-id="edd9b-1922">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="edd9b-1922">Method literals</span></span>

    public int literals([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1923">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1923">Parameters</span></span>

<span data-ttu-id="edd9b-1924">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1924">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1925">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1925">Return Value</span></span>

### <a name="method-loadcsv"></a><span data-ttu-id="edd9b-1926">メソッド loadCsv</span><span class="sxs-lookup"><span data-stu-id="edd9b-1926">Method loadCsv</span></span>

    public Guid loadCsv(str fileName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1927">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1927">Parameters</span></span>

<span data-ttu-id="edd9b-1928">fileName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1928">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1929">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1929">Return Value</span></span>

### <a name="method-loadxml"></a><span data-ttu-id="edd9b-1930">メソッド loadXml</span><span class="sxs-lookup"><span data-stu-id="edd9b-1930">Method loadXml</span></span>

    public Guid loadXml(str fileName)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1931">Parameters</span></span>

<span data-ttu-id="edd9b-1932">fileName</span><span class="sxs-lookup"><span data-stu-id="edd9b-1932">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1933">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1933">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="edd9b-1934">メソッド名</span><span class="sxs-lookup"><span data-stu-id="edd9b-1934">Method name</span></span>

<span data-ttu-id="edd9b-1935">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1935">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1936">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1936">Parameters</span></span>

<span data-ttu-id="edd9b-1937">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1937">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1938">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1938">Return Value</span></span>

<span data-ttu-id="edd9b-1939">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1939">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1940">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1940">Remarks</span></span>

<span data-ttu-id="edd9b-1941">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1941">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="edd9b-1942">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1942">Begins with a letter.</span></span>
-   <span data-ttu-id="edd9b-1943">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1943">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="edd9b-1944">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1944">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="edd9b-1945">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1945">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="edd9b-1946">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1946">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-newobject"></a><span data-ttu-id="edd9b-1947">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="edd9b-1947">Method newObject</span></span>

    public QueryRun newObject(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="edd9b-1948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1948">Parameters</span></span>

<span data-ttu-id="edd9b-1949">ソース</span><span class="sxs-lookup"><span data-stu-id="edd9b-1949">source</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1950">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1950">Return Value</span></span>

### <a name="method-next"></a><span data-ttu-id="edd9b-1951">メソッド next</span><span class="sxs-lookup"><span data-stu-id="edd9b-1951">Method next</span></span>

<span data-ttu-id="edd9b-1952">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1952">Retrieves the next record from the query.</span></span>

    public boolean next()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1953">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1953">Return Value</span></span>

<span data-ttu-id="edd9b-1954">次のレコードが利用可能で getNo メソッドまたは get メソッドで取得することができる場合は true。クエリ内に設定された制約を満たすレコードがそれ以上存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1954">true if the next record is available and can be fetched with the getNo method or get method; false if no there are no more records that satisfy the constraint set up in the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1955">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1955">Remarks</span></span>

<span data-ttu-id="edd9b-1956">変更されたメソッドまたは changedNo メソッドを使用して、指定されたデータ ソースのレコードが前回の次のメソッド呼び出しから変更されたかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1956">The changed method or changedNo method can be used to check whether the record from the given data source has changed since the previous call to the next method.</span></span>

#### <a name="examples"></a><span data-ttu-id="edd9b-1957">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1957">Examples</span></span>

    { 
        queryRun qr; 
        CustTable ct; 
        // ... 
        if (qr.prompt()) 
        { 
            while (qr.next()) 
            { 
                if (qr.Changed(tableNum(CustTable))) 
                { 
                    ct = qr.Get (tableNum(CustTable)); 
                    print ct.AccountNum; 
                } 
            } 
        } 
    }

### <a name="method-nextuniqueid"></a><span data-ttu-id="edd9b-1958">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="edd9b-1958">Method nextUniqueId</span></span>

    public int nextUniqueId([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1959">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1959">Parameters</span></span>

<span data-ttu-id="edd9b-1960">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1960">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1961">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1961">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="edd9b-1962">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="edd9b-1962">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1963">Parameters</span></span>

<span data-ttu-id="edd9b-1964">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1964">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1965">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1965">Return Value</span></span>

### <a name="method-pack"></a><span data-ttu-id="edd9b-1966">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="edd9b-1966">Method pack</span></span>

    public container pack([boolean doCheck])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1967">Parameters</span></span>

<span data-ttu-id="edd9b-1968">doCheck</span><span class="sxs-lookup"><span data-stu-id="edd9b-1968">doCheck</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1969">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1969">Return Value</span></span>

### <a name="method-prompt"></a><span data-ttu-id="edd9b-1970">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="edd9b-1970">Method prompt</span></span>

<span data-ttu-id="edd9b-1971">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1971">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>

    public boolean prompt()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1972">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1972">Return Value</span></span>

<span data-ttu-id="edd9b-1973">ユーザーが OK をクリックして検索が続行される場合は true。ユーザーがキャンセルをクリックして検索を停止した場合は false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1973">true if the user clicked OK and the search is to continue; false if the user clicked Cancel to stop the search.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-1974">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-1974">Remarks</span></span>

<span data-ttu-id="edd9b-1975">ユーザーには、フェッチされたレコードによって実行される制約を定義する範囲を与えるためのフォームが提示される。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1975">The user is presented with a form to give ranges that define constraints to be fulfilled by the fetched records.</span></span> <span data-ttu-id="edd9b-1976">または、ユーザーは新しいフィールドを追加し、区切ったり、変更したり、並べ替えたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1976">Or the user may add new fields to delimit, change the sorting, and so on.</span></span> <span data-ttu-id="edd9b-1977">このメソッドをオーバーロードすると、事前定義されたクエリ フォームではなく、アプリケーション定義の方法でユーザーにプロンプトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1977">This method can be overloaded to prompt the user in an application-defined way instead of in through the predefined query form.</span></span> <span data-ttu-id="edd9b-1978">または、この方法は、フェッチされるレコードをユーザーがコントロールできないように、オーバーロードされることがあります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1978">Or this method can be overloaded to avoid giving the user control over which records are fetched.</span></span> <span data-ttu-id="edd9b-1979">これらの結果を生成するには、継承したメソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1979">To produce these results, do not call the inherited method.</span></span> <span data-ttu-id="edd9b-1980">いずれの場合でも、関数はクエリが続行する場合は true、それ以外の場合は false を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-1980">In any case, the function should return true if the query is to continue, and false otherwise.</span></span>

#### <a name="examples"></a><span data-ttu-id="edd9b-1981">例</span><span class="sxs-lookup"><span data-stu-id="edd9b-1981">Examples</span></span>

    { 
        QueryRun qr; 
        // ... 
        if (qr.prompt()) 
        { 
            // The user pressed OK. Go ahead and do whatever is required. 
        } 
        else 
        { 
            // The user pressed Cancel. 
        } 
    }

### <a name="method-query"></a><span data-ttu-id="edd9b-1982">メソッド query</span><span class="sxs-lookup"><span data-stu-id="edd9b-1982">Method query</span></span>

    public Query query([Query query])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1983">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1983">Parameters</span></span>

<span data-ttu-id="edd9b-1984">クエリ</span><span class="sxs-lookup"><span data-stu-id="edd9b-1984">query</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1985">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1985">Return Value</span></span>

### <a name="method-querytype"></a><span data-ttu-id="edd9b-1986">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="edd9b-1986">Method queryType</span></span>

    public int queryType([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1987">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1987">Parameters</span></span>

<span data-ttu-id="edd9b-1988">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1988">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1989">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1989">Return Value</span></span>

### <a name="method-recordlevelsecurity"></a><span data-ttu-id="edd9b-1990">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="edd9b-1990">Method recordLevelSecurity</span></span>

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-1991">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-1991">Parameters</span></span>

<span data-ttu-id="edd9b-1992">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1992">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-1993">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1993">Return Value</span></span>

### <a name="method-report"></a><span data-ttu-id="edd9b-1994">メソッド report</span><span class="sxs-lookup"><span data-stu-id="edd9b-1994">Method report</span></span>

    public ReportRun report()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1995">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1995">Return Value</span></span>

### <a name="method-reportrun"></a><span data-ttu-id="edd9b-1996">メソッド reportRun</span><span class="sxs-lookup"><span data-stu-id="edd9b-1996">Method reportRun</span></span>

    public ReportRun reportRun()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1997">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1997">Return Value</span></span>

### <a name="method-saved"></a><span data-ttu-id="edd9b-1998">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="edd9b-1998">Method saved</span></span>

    public boolean saved()

#### <a name="return-value"></a><span data-ttu-id="edd9b-1999">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-1999">Return Value</span></span>

### <a name="method-saveusersetup"></a><span data-ttu-id="edd9b-2000">メソッド saveUserSetup</span><span class="sxs-lookup"><span data-stu-id="edd9b-2000">Method saveUserSetup</span></span>

<span data-ttu-id="edd9b-2001">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2001">Saves the user setup.</span></span>

    public boolean saveUserSetup([boolean saveIt])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2002">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2002">Parameters</span></span>

<span data-ttu-id="edd9b-2003">saveIt</span><span class="sxs-lookup"><span data-stu-id="edd9b-2003">saveIt</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2004">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2004">Return Value</span></span>

<span data-ttu-id="edd9b-2005">設定が正常に保存された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2005">true if the setup was successfully saved; otherwise false.</span></span>

### <a name="method-searchable"></a><span data-ttu-id="edd9b-2006">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="edd9b-2006">Method searchable</span></span>

    public boolean searchable([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2007">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2007">Parameters</span></span>

<span data-ttu-id="edd9b-2008">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2008">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2009">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2009">Return Value</span></span>

### <a name="method-setcursor"></a><span data-ttu-id="edd9b-2010">メソッド setCursor</span><span class="sxs-lookup"><span data-stu-id="edd9b-2010">Method setCursor</span></span>

    public boolean setCursor(Common record, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2011">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2011">Parameters</span></span>

<span data-ttu-id="edd9b-2012">記録</span><span class="sxs-lookup"><span data-stu-id="edd9b-2012">record</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2013">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-2013">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2014">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2014">Return Value</span></span>

### <a name="method-setrecord"></a><span data-ttu-id="edd9b-2015">メソッド setRecord</span><span class="sxs-lookup"><span data-stu-id="edd9b-2015">Method setRecord</span></span>

    public boolean setRecord(Common record, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2016">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2016">Parameters</span></span>

<span data-ttu-id="edd9b-2017">記録</span><span class="sxs-lookup"><span data-stu-id="edd9b-2017">record</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2018">occurrence</span><span class="sxs-lookup"><span data-stu-id="edd9b-2018">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2019">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2019">Return Value</span></span>

### <a name="method-title"></a><span data-ttu-id="edd9b-2020">メソッド title</span><span class="sxs-lookup"><span data-stu-id="edd9b-2020">Method title</span></span>

    public str title([str value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2021">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2021">Parameters</span></span>

<span data-ttu-id="edd9b-2022">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2022">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2023">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2023">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="edd9b-2024">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="edd9b-2024">Method toString</span></span>

<span data-ttu-id="edd9b-2025">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2025">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="edd9b-2026">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2026">Return Value</span></span>

<span data-ttu-id="edd9b-2027">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2027">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="edd9b-2028">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-2028">Remarks</span></span>

<span data-ttu-id="edd9b-2029">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2029">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="edd9b-2030">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2030">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="edd9b-2031">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2031">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-userupdate"></a><span data-ttu-id="edd9b-2032">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="edd9b-2032">Method userUpdate</span></span>

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2033">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2033">Parameters</span></span>

<span data-ttu-id="edd9b-2034">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2034">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2035">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2035">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="edd9b-2036">メソッド version</span><span class="sxs-lookup"><span data-stu-id="edd9b-2036">Method version</span></span>

    public int version([int value])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2037">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2037">Parameters</span></span>

<span data-ttu-id="edd9b-2038">値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2038">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2039">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2039">Return Value</span></span>

### <a name="method-getqueryrowcount"></a><span data-ttu-id="edd9b-2040">メソッド getQueryRowCount</span><span class="sxs-lookup"><span data-stu-id="edd9b-2040">Method getQueryRowCount</span></span>

    public static int getQueryRowCount(Query query, int maxRows)

#### <a name="parameters"></a><span data-ttu-id="edd9b-2041">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2041">Parameters</span></span>

<span data-ttu-id="edd9b-2042">クエリ</span><span class="sxs-lookup"><span data-stu-id="edd9b-2042">query</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2043">maxRows</span><span class="sxs-lookup"><span data-stu-id="edd9b-2043">maxRows</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2044">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2044">Return Value</span></span>

### <a name="method-runandpopulate"></a><span data-ttu-id="edd9b-2045">メソッド runAndPopulate</span><span class="sxs-lookup"><span data-stu-id="edd9b-2045">Method runAndPopulate</span></span>

    public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)

#### <a name="parameters"></a><span data-ttu-id="edd9b-2046">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2046">Parameters</span></span>

<span data-ttu-id="edd9b-2047">sourceRuery</span><span class="sxs-lookup"><span data-stu-id="edd9b-2047">sourceRuery</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2048">targetTable</span><span class="sxs-lookup"><span data-stu-id="edd9b-2048">targetTable</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2049">queryAliasesAndTargetColumnsMap</span><span class="sxs-lookup"><span data-stu-id="edd9b-2049">queryAliasesAndTargetColumnsMap</span></span>  

#### <a name="return-value"></a><span data-ttu-id="edd9b-2050">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2050">Return Value</span></span>

### <a name="method-run"></a><span data-ttu-id="edd9b-2051">メソッド run</span><span class="sxs-lookup"><span data-stu-id="edd9b-2051">Method run</span></span>

<span data-ttu-id="edd9b-2052">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2052">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>

    public void run()

#### <a name="remarks"></a><span data-ttu-id="edd9b-2053">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-2053">Remarks</span></span>

<span data-ttu-id="edd9b-2054">クエリを実行すると、ユーザーによって入力された制約を満たすレコードが検索されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2054">Running the query will find the records that satisfy the constraints entered by the user.</span></span> <span data-ttu-id="edd9b-2055">ただし、この方法でのクエリの実行には副作用がありません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2055">However, running the query in this manner has no side effects.</span></span> <span data-ttu-id="edd9b-2056">扱いやすくするために、1 つ以上の継承されたメソッドをオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2056">In order to be useful, one or more of the inherited methods must be overloaded.</span></span>

### <a name="method-new"></a><span data-ttu-id="edd9b-2057">メソッド new</span><span class="sxs-lookup"><span data-stu-id="edd9b-2057">Method new</span></span>

<span data-ttu-id="edd9b-2058">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2058">Initializes a new instance of the Object class.</span></span>

    public void new(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="edd9b-2059">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2059">Parameters</span></span>

<span data-ttu-id="edd9b-2060">ソース</span><span class="sxs-lookup"><span data-stu-id="edd9b-2060">source</span></span>  

#### <a name="remarks"></a><span data-ttu-id="edd9b-2061">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-2061">Remarks</span></span>

<span data-ttu-id="edd9b-2062">クエリ クラスのインスタンスを QueryRun クラスのコンストラクターに渡すと、クエリ オブジェクトのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2062">When you pass an instance of the Query class into this constructor of the QueryRun class, a copy of the Query object is created.</span></span> <span data-ttu-id="edd9b-2063">このクエリ オブジェクト のコピーに加えられた変更は、元のクエリ オブジェクトには影響しません。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2063">Changes that are made to this copy of the Query object do not affect the original Query object.</span></span>

### <a name="method-addpagerange"></a><span data-ttu-id="edd9b-2064">メソッド addPageRange</span><span class="sxs-lookup"><span data-stu-id="edd9b-2064">Method addPageRange</span></span>

    public void addPageRange([Int64 startingPosition], [Int64 numberOfRecordsToFetch])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2065">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2065">Parameters</span></span>

<span data-ttu-id="edd9b-2066">startingPosition</span><span class="sxs-lookup"><span data-stu-id="edd9b-2066">startingPosition</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2067">numberOfRecordsToFetch</span><span class="sxs-lookup"><span data-stu-id="edd9b-2067">numberOfRecordsToFetch</span></span>  

### <a name="method-reset"></a><span data-ttu-id="edd9b-2068">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="edd9b-2068">Method reset</span></span>

    public void reset()

### <a name="method-setimportsession"></a><span data-ttu-id="edd9b-2069">メソッド setImportSession</span><span class="sxs-lookup"><span data-stu-id="edd9b-2069">Method setImportSession</span></span>

    public void setImportSession(Guid importSession)

#### <a name="parameters"></a><span data-ttu-id="edd9b-2070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2070">Parameters</span></span>

<span data-ttu-id="edd9b-2071">importSession</span><span class="sxs-lookup"><span data-stu-id="edd9b-2071">importSession</span></span>  

### <a name="method-setquerytimeout"></a><span data-ttu-id="edd9b-2072">メソッド setQuerytimeout</span><span class="sxs-lookup"><span data-stu-id="edd9b-2072">Method setQuerytimeout</span></span>

    public void setQuerytimeout(int seconds, [boolean raiseException])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2073">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2073">Parameters</span></span>

<span data-ttu-id="edd9b-2074"> 秒</span><span class="sxs-lookup"><span data-stu-id="edd9b-2074">seconds</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2075">raiseException</span><span class="sxs-lookup"><span data-stu-id="edd9b-2075">raiseException</span></span>  

### <a name="method-init"></a><span data-ttu-id="edd9b-2076">メソッド init</span><span class="sxs-lookup"><span data-stu-id="edd9b-2076">Method init</span></span>

    public void init()

### <a name="method-enablepositionpaging"></a><span data-ttu-id="edd9b-2077">メソッド enablePositionPaging</span><span class="sxs-lookup"><span data-stu-id="edd9b-2077">Method enablePositionPaging</span></span>

    public void enablePositionPaging([boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2078">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2078">Parameters</span></span>

<span data-ttu-id="edd9b-2079">有効</span><span class="sxs-lookup"><span data-stu-id="edd9b-2079">enabled</span></span>  

### <a name="method-shred"></a><span data-ttu-id="edd9b-2080">メソッド shred</span><span class="sxs-lookup"><span data-stu-id="edd9b-2080">Method shred</span></span>

    public void shred(Guid importSession)

#### <a name="parameters"></a><span data-ttu-id="edd9b-2081">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2081">Parameters</span></span>

<span data-ttu-id="edd9b-2082">importSession</span><span class="sxs-lookup"><span data-stu-id="edd9b-2082">importSession</span></span>  

### <a name="method-enablevaluebasedpaging"></a><span data-ttu-id="edd9b-2083">メソッド enableValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="edd9b-2083">Method enableValueBasedPaging</span></span>

    public void enableValueBasedPaging([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2084">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2084">Parameters</span></span>

<span data-ttu-id="edd9b-2085">enable</span><span class="sxs-lookup"><span data-stu-id="edd9b-2085">enable</span></span>  

### <a name="method-bulknext"></a><span data-ttu-id="edd9b-2086">メソッド bulkNext</span><span class="sxs-lookup"><span data-stu-id="edd9b-2086">Method bulkNext</span></span>

    public void bulkNext([boolean fetchAllData])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2087">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2087">Parameters</span></span>

<span data-ttu-id="edd9b-2088">fetchAllData</span><span class="sxs-lookup"><span data-stu-id="edd9b-2088">fetchAllData</span></span>  

### <a name="method-applyvaluebasedpaging"></a><span data-ttu-id="edd9b-2089">メソッド applyValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="edd9b-2089">Method applyValueBasedPaging</span></span>

    public void applyValueBasedPaging([Common sourceCursor], [boolean isForward])

#### <a name="parameters"></a><span data-ttu-id="edd9b-2090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2090">Parameters</span></span>

<span data-ttu-id="edd9b-2091">sourceCursor</span><span class="sxs-lookup"><span data-stu-id="edd9b-2091">sourceCursor</span></span>  

<!-- -->

<span data-ttu-id="edd9b-2092">isForward</span><span class="sxs-lookup"><span data-stu-id="edd9b-2092">isForward</span></span>  

### <a name="method-skipautoorderby"></a><span data-ttu-id="edd9b-2093">メソッド skipAutoOrderBy</span><span class="sxs-lookup"><span data-stu-id="edd9b-2093">Method skipAutoOrderBy</span></span>

    Specifies whether an Order By clause will be generated, in case no Order By field was specified.
    public boolean skipAutoOrderBy([boolean value])
    
#### <a name="parameters"></a><span data-ttu-id="edd9b-2094">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edd9b-2094">Parameters</span></span>
<span data-ttu-id="edd9b-2095">金額</span><span class="sxs-lookup"><span data-stu-id="edd9b-2095">Value</span></span>
#### <a name="return-value"></a><span data-ttu-id="edd9b-2096">戻り値</span><span class="sxs-lookup"><span data-stu-id="edd9b-2096">Return Value</span></span>
<span data-ttu-id="edd9b-2097">パラメーターが指定されていない場合は現在の値、パラメーターが指定されている場合は新しい値です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2097">The current value if no parameter is specified, the new value if a parameter was specified.</span></span>
#### <a name="remarks"></a><span data-ttu-id="edd9b-2098">備考</span><span class="sxs-lookup"><span data-stu-id="edd9b-2098">Remarks</span></span>
<span data-ttu-id="edd9b-2099">既定では SkipAutoOrderBy は false で、プラットフォーム更新プログラム 31 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="edd9b-2099">SkipAutoOrderBy is false by default and available in Platform update 31 and later</span></span>
