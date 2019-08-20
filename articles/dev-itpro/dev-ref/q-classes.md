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
ms.openlocfilehash: 159432f6ecdab9ba06ec2ee86d18c37a2413a5a5
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833678"
---
# <a name="q-classes"></a><span data-ttu-id="26fa0-103">Q クラス</span><span class="sxs-lookup"><span data-stu-id="26fa0-103">Q classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26fa0-104">文字 Q で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="26fa0-104">System API classes that start with the letter Q.</span></span>

<a name="class-query"></a><span data-ttu-id="26fa0-105">クラス クエリ</span><span class="sxs-lookup"><span data-stu-id="26fa0-105">Class Query</span></span>
-----------

    class Query extends TreeNode

<span data-ttu-id="26fa0-106">クエリ クラスには、クエリの構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-106">The Query class embodies the structure of a query.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-107">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-107">Remarks</span></span>

<span data-ttu-id="26fa0-108">このタイプのオブジェクトは、データベースからレコードをフェッチするために使用されません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-108">Objects of this kind are not used to fetch records from the database.</span></span> <span data-ttu-id="26fa0-109">代わりに、クエリ オブジェクトを割り当てることができる QueryRun オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-109">Instead, use a QueryRun object that can be assigned a query object.</span></span> <span data-ttu-id="26fa0-110">クエリの動的な動作は、QueryRun クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-110">The dynamic behavior of a query is defined by the QueryRun class.</span></span> <span data-ttu-id="26fa0-111">静的なビヘイビアーは、Query クラスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-111">The static behavior is defined by the Query class.</span></span> <span data-ttu-id="26fa0-112">クエリには、データベース内のテーブルに対応する 1 つまたは複数のデータ ソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-112">Queries contain one or more data sources that correspond to tables in the database.</span></span> <span data-ttu-id="26fa0-113">データ ソースを指定するには、QueryBuildDataSource オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-113">The data sources are specified by using QueryBuildDataSource objects.</span></span> <span data-ttu-id="26fa0-114">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-114">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="26fa0-115">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-115">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="26fa0-116">クエリは、ユーザーが、たとえばフォームなどによりフェッチされるレコードを変更する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-116">Queries are used when the user wants to modify the records that are fetched by, for example, a form.</span></span> <span data-ttu-id="26fa0-117">多くの場合、1 つ以上の範囲は既存のデータ ソースに追加されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-117">One or more ranges are often added to an existing data source.</span></span> <span data-ttu-id="26fa0-118">範囲を指定するには、queryBuildRange オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-118">Ranges are specified by using queryBuildRange objects.</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-119">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-119">Examples</span></span>

<span data-ttu-id="26fa0-120">次の例では、QueryRun オブジェクトを作成するために使用されるクエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-120">The following example creates a query object that is used to create a QueryRun object.</span></span>

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

### <a name="methods"></a><span data-ttu-id="26fa0-121">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-121">Methods</span></span>

| <span data-ttu-id="26fa0-122">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-122">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="26fa0-123">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-123">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fa0-124">public Query addBaseQuery(str queryName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-124">public Query addBaseQuery(str queryName)</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-125">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-125">public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])</span></span>                                            | <span data-ttu-id="26fa0-126">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-126">Adds a data source to the top level of the query.</span></span>                                                                                         |
| <span data-ttu-id="26fa0-127">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-127">public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])</span></span>                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-128">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-128">public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-129">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-129">public boolean allowCheck(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-130">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-130">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-131">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span><span class="sxs-lookup"><span data-stu-id="26fa0-131">public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-132">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="26fa0-132">public boolean allowQueryFilters(QueryBuildDataSource dataSource)</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-133">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-133">public str changedBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="26fa0-134">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-134">Gets or sets the name of the user who last changed the Query object.</span></span>                                                                      |
| <span data-ttu-id="26fa0-135">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-135">public Date changedDate(\[Date value\])</span></span>                                                                                                                                | <span data-ttu-id="26fa0-136">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-136">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="26fa0-137">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-137">public str changedTime(\[str value\])</span></span>                                                                                                                                  | <span data-ttu-id="26fa0-138">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-138">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="26fa0-139">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-139">public int childDataSourceCount()</span></span>                                                                                                                                      | <span data-ttu-id="26fa0-140">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-140">Counts the number of data sources that are related to the query.</span></span>                                                                          |
| <span data-ttu-id="26fa0-141">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-141">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                                        | <span data-ttu-id="26fa0-142">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-142">Returns the child data source that corresponds to the specified number.</span></span>                                                                   |
| <span data-ttu-id="26fa0-143">public boolean containsAggregateFields()</span><span class="sxs-lookup"><span data-stu-id="26fa0-143">public boolean containsAggregateFields()</span></span>                                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-144">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-144">public str createdBy(\[str value\])</span></span>                                                                                                                                    | <span data-ttu-id="26fa0-145">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-145">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="26fa0-146">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-146">public Date creationDate(\[Date value\])</span></span>                                                                                                                               | <span data-ttu-id="26fa0-147">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-147">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="26fa0-148">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-148">public str creationTime(\[str value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-149">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-149">public int dataSourceCount()</span></span>                                                                                                                                           | <span data-ttu-id="26fa0-150">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-150">Returns the total number of data sources for the query, including any embedded data sources.</span></span>                                              |
| <span data-ttu-id="26fa0-151">public QueryBuildDataSource dataSourceName(str name)</span><span class="sxs-lookup"><span data-stu-id="26fa0-151">public QueryBuildDataSource dataSourceName(str name)</span></span>                                                                                                                   | <span data-ttu-id="26fa0-152">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-152">Returns the data source that has the specified name.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-153">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-153">public QueryBuildDataSource dataSourceNo(int dataSourceNo)</span></span>                                                                                                             | <span data-ttu-id="26fa0-154">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-154">Returns the data source that is specified by the data source number.</span></span>                                                                      |
| <span data-ttu-id="26fa0-155">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-155">public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])</span></span>                                                                                         | <span data-ttu-id="26fa0-156">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-156">Returns the data source that the specified table is assigned to.</span></span>                                                                          |
| <span data-ttu-id="26fa0-157">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span><span class="sxs-lookup"><span data-stu-id="26fa0-157">public QueryBuildDataSource dataSourceUniqueId(int uniqueId)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-158">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-158">public str description(\[str value\])</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-159">public boolean equal(Object record)</span><span class="sxs-lookup"><span data-stu-id="26fa0-159">public boolean equal(Object record)</span></span>                                                                                                                                    | <span data-ttu-id="26fa0-160">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-160">Evaluates whether one query is equal to another.</span></span>                                                                                          |
| <span data-ttu-id="26fa0-161">public str exportXML()</span><span class="sxs-lookup"><span data-stu-id="26fa0-161">public str exportXML()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-162">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-162">public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-163">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-163">public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-164">public QueryBuildDataSource firstTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-164">public QueryBuildDataSource firstTopLevelDataSource()</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-165">public boolean forceNestedLoop(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="26fa0-165">public boolean forceNestedLoop(boolean arg)</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-166">public boolean forceSelectOrder(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="26fa0-166">public boolean forceSelectOrder(boolean arg)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-167">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-167">public str form(\[str value\])</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-168">public container getCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="26fa0-168">public container getCompanyRange()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-169">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-169">public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-170">public int getNextUniqueId()</span><span class="sxs-lookup"><span data-stu-id="26fa0-170">public int getNextUniqueId()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-171">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-171">public str getSQLStatement(\[boolean noRuntimeOptimization\])</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-172">public container getValidTimeStateDateRange()</span><span class="sxs-lookup"><span data-stu-id="26fa0-172">public container getValidTimeStateDateRange()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-173">public container getValidTimeStateDateTimeRange()</span><span class="sxs-lookup"><span data-stu-id="26fa0-173">public container getValidTimeStateDateTimeRange()</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-174">public ValidTimeStateQueryType getValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="26fa0-174">public ValidTimeStateQueryType getValidTimeStateQueryType()</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-175">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-175">public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-176">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-176">public int groupByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-177">public boolean hasMultipleTopLevelDataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-177">public boolean hasMultipleTopLevelDataSource()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-178">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span><span class="sxs-lookup"><span data-stu-id="26fa0-178">public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)</span></span>                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-179">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-179">public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-180">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-180">public int havingFilterCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-181">public boolean inReport()</span><span class="sxs-lookup"><span data-stu-id="26fa0-181">public boolean inReport()</span></span>                                                                                                                                              | <span data-ttu-id="26fa0-182">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-182">Determines whether the query is part of a report.</span></span>                                                                                         |
| <span data-ttu-id="26fa0-183">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-183">public boolean interactive(\[boolean value\])</span></span>                                                                                                                          | <span data-ttu-id="26fa0-184">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-184">Specifies whether the query is interactive.</span></span>                                                                                               |
| <span data-ttu-id="26fa0-185">public boolean isCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="26fa0-185">public boolean isCompositeQuery()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-186">public boolean isExplicitlyOrdered()</span><span class="sxs-lookup"><span data-stu-id="26fa0-186">public boolean isExplicitlyOrdered()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-187">public boolean isExplicitlyGrouped()</span><span class="sxs-lookup"><span data-stu-id="26fa0-187">public boolean isExplicitlyGrouped()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-188">public boolean isPureUnionAll()</span><span class="sxs-lookup"><span data-stu-id="26fa0-188">public boolean isPureUnionAll()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-189">public boolean isUnionType()</span><span class="sxs-lookup"><span data-stu-id="26fa0-189">public boolean isUnionType()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-190">public int levelNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-190">public int levelNo(int dataSourceNo)</span></span>                                                                                                                                   | <span data-ttu-id="26fa0-191">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-191">Determines the level of indentation of the specified data source.</span></span>                                                                         |
| <span data-ttu-id="26fa0-192">public int levelTable(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-192">public int levelTable(TableId table, \[int occurrence\])</span></span>                                                                                                               | <span data-ttu-id="26fa0-193">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-193">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>                  |
| <span data-ttu-id="26fa0-194">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-194">public int literals(\[int value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-195">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-195">public str name(\[str value\])</span></span>                                                                                                                                         | <span data-ttu-id="26fa0-196">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-196">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="26fa0-197">public Query newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="26fa0-197">public Query newObject(AnyType source)</span></span>                                                                                                                                 | <span data-ttu-id="26fa0-198">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-198">Creates a query that exists on the same client side or server side as the source query.</span></span>                                                   |
| <span data-ttu-id="26fa0-199">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-199">public int nextUniqueId(\[int value\])</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-200">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-200">public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-201">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-201">public int orderByFieldCount(\[QueryBuildDataSource dataSource\])</span></span>                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-202">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-202">public Guid origin(\[Guid value\])</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-203">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-203">public container pack(\[boolean doCheck\])</span></span>                                                                                                                             | <span data-ttu-id="26fa0-204">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-204">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>                              |
| <span data-ttu-id="26fa0-205">public container packInternals()</span><span class="sxs-lookup"><span data-stu-id="26fa0-205">public container packInternals()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-206">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-206">public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])</span></span>                                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-207">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-207">public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-208">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-208">public int queryType(\[int value\])</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-209">public str quickFilterValue()</span><span class="sxs-lookup"><span data-stu-id="26fa0-209">public str quickFilterValue()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-210">public int quickFilterControlId()</span><span class="sxs-lookup"><span data-stu-id="26fa0-210">public int quickFilterControlId()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-211">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-211">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-212">public Report report()</span><span class="sxs-lookup"><span data-stu-id="26fa0-212">public Report report()</span></span>                                                                                                                                                 | <span data-ttu-id="26fa0-213">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-213">Returns the report in which the query is defined, if the report exists.</span></span>                                                                   |
| <span data-ttu-id="26fa0-214">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="26fa0-214">public boolean saved()</span></span>                                                                                                                                                 | <span data-ttu-id="26fa0-215">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-215">Indicates whether the query has been saved to disk.</span></span>                                                                                       |
| <span data-ttu-id="26fa0-216">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-216">public boolean searchable(\[boolean value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-217">public Guid importSession(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-217">public Guid importSession(\[Guid value\])</span></span>                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-218">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-218">public str title(\[str value\])</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-219">public int topRows(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-219">public int topRows(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-220">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-220">public str toString()</span></span>                                                                                                                                                  | <span data-ttu-id="26fa0-221">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-221">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-222">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-222">public boolean userUpdate(\[boolean value\])</span></span>                                                                                                                           | <span data-ttu-id="26fa0-223">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-223">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>                                             |
| <span data-ttu-id="26fa0-224">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-224">public Date validTimeStateAsOfDate(\[Date asOfDate\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-225">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-225">public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])</span></span>                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-226">public int validTimeStateFlags(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-226">public int validTimeStateFlags(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-227">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-227">public int version(\[int value\])</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-228">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-228">public str xml(\[int indent\])</span></span>                                                                                                                                         | <span data-ttu-id="26fa0-229">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-229">Returns an XML string that represents the current object.</span></span>                                                                                 |
| <span data-ttu-id="26fa0-230">public void clearBaseQueries()</span><span class="sxs-lookup"><span data-stu-id="26fa0-230">public void clearBaseQueries()</span></span>                                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-231">public void addCompanyRange(str companyName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-231">public void addCompanyRange(str companyName)</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-232">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span><span class="sxs-lookup"><span data-stu-id="26fa0-232">public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-233">public void clearCompanyRange()</span><span class="sxs-lookup"><span data-stu-id="26fa0-233">public void clearCompanyRange()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-234">public void unpackInternals(container internalData)</span><span class="sxs-lookup"><span data-stu-id="26fa0-234">public void unpackInternals(container internalData)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-235">public void new(\[AnyType source\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-235">public void new(\[AnyType source\])</span></span>                                                                                                                                    | <span data-ttu-id="26fa0-236">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-236">Creates a query object.</span></span>                                                                                                                   |
| <span data-ttu-id="26fa0-237">public void checkFieldAccess(boolean setCheckFieldAccess)</span><span class="sxs-lookup"><span data-stu-id="26fa0-237">public void checkFieldAccess(boolean setCheckFieldAccess)</span></span>                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-238">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-238">public void useDbCacheOnGeneratedCursors(\[int fetchsize\])</span></span>                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-239">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-239">public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])</span></span>                                                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-240">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-240">public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-241">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-241">public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-242">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-242">public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-243">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-243">public void finalize()</span></span>                                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-244">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-244">public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-245">public void clearOrderBy()</span><span class="sxs-lookup"><span data-stu-id="26fa0-245">public void clearOrderBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-246">public void clearAllFields()</span><span class="sxs-lookup"><span data-stu-id="26fa0-246">public void clearAllFields()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-247">public void clearGroupBy()</span><span class="sxs-lookup"><span data-stu-id="26fa0-247">public void clearGroupBy()</span></span>                                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-248">public void autoAuthzMode(AutoAuthzMode mode)</span><span class="sxs-lookup"><span data-stu-id="26fa0-248">public void autoAuthzMode(AutoAuthzMode mode)</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-249">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span><span class="sxs-lookup"><span data-stu-id="26fa0-249">::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-250">public void generateCursors()</span><span class="sxs-lookup"><span data-stu-id="26fa0-250">public void generateCursors()</span></span>                                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-251">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span><span class="sxs-lookup"><span data-stu-id="26fa0-251">public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-252">public void addContains(str containsValue, \[boolean prefixSearch\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-252">public void addContains(str containsValue, \[boolean prefixSearch\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-253">public void resetValidTimeStateQueryType()</span><span class="sxs-lookup"><span data-stu-id="26fa0-253">public void resetValidTimeStateQueryType()</span></span>                                                                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-254">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-254">public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])</span></span>                                                                            |                                                                                                                                           |

### <a name="method-addbasequery"></a><span data-ttu-id="26fa0-255">メソッド addBaseQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-255">Method addBaseQuery</span></span>

    public Query addBaseQuery(str queryName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-256">Parameters</span></span>

<span data-ttu-id="26fa0-257">queryName</span><span class="sxs-lookup"><span data-stu-id="26fa0-257">queryName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-258">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-258">Return Value</span></span>

### <a name="method-adddatasource"></a><span data-ttu-id="26fa0-259">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-259">Method addDataSource</span></span>

<span data-ttu-id="26fa0-260">クエリのトップ レベルにデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-260">Adds a data source to the top level of the query.</span></span>

    public QueryBuildDataSource addDataSource(TableId table, [str name], [UnionType unionType], [boolean emptyFieldList])

#### <a name="parameters"></a><span data-ttu-id="26fa0-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-261">Parameters</span></span>

<span data-ttu-id="26fa0-262">テーブル</span><span class="sxs-lookup"><span data-stu-id="26fa0-262">table</span></span>  

<!-- -->

<span data-ttu-id="26fa0-263">名前</span><span class="sxs-lookup"><span data-stu-id="26fa0-263">name</span></span>  

<!-- -->

<span data-ttu-id="26fa0-264">unionType</span><span class="sxs-lookup"><span data-stu-id="26fa0-264">unionType</span></span>  

<!-- -->

<span data-ttu-id="26fa0-265">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="26fa0-265">emptyFieldList</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-266">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-266">Return Value</span></span>

<span data-ttu-id="26fa0-267">作成されたデータ ソース オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="26fa0-267">The data source object that is created.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-268">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-268">Remarks</span></span>

<span data-ttu-id="26fa0-269">文書作成のために名前の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-269">A name value can be specified for documentation purposes.</span></span> <span data-ttu-id="26fa0-270">dataSourceName メソッドを使用してデータ ソースをフェッチする名前を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-270">You can use the name to fetch the data source by using the dataSourceName method.</span></span>

### <a name="method-addhavingfilter"></a><span data-ttu-id="26fa0-271">メソッド addHavingFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-271">Method addHavingFilter</span></span>

    public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-272">Parameters</span></span>

<span data-ttu-id="26fa0-273">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-273">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-274">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-274">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-275">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="26fa0-275">aggregateFunction</span></span>  

<!-- -->

<span data-ttu-id="26fa0-276">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-276">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-277">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-277">Return Value</span></span>

### <a name="method-addqueryfilter"></a><span data-ttu-id="26fa0-278">メソッド addQueryFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-278">Method addQueryFilter</span></span>

    public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-279">Parameters</span></span>

<span data-ttu-id="26fa0-280">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-280">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-281">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-281">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-282">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-282">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-283">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-283">Return Value</span></span>

### <a name="method-allowcheck"></a><span data-ttu-id="26fa0-284">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="26fa0-284">Method allowCheck</span></span>

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-285">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-285">Parameters</span></span>

<span data-ttu-id="26fa0-286">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-286">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-287">Return Value</span></span>

### <a name="method-allowcrosscompany"></a><span data-ttu-id="26fa0-288">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="26fa0-288">Method allowCrossCompany</span></span>

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-289">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-289">Parameters</span></span>

<span data-ttu-id="26fa0-290">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-290">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-291">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-291">Return Value</span></span>

### <a name="method-allowhavingfilters"></a><span data-ttu-id="26fa0-292">メソッド allowHavingFilters</span><span class="sxs-lookup"><span data-stu-id="26fa0-292">Method allowHavingFilters</span></span>

    public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)

#### <a name="parameters"></a><span data-ttu-id="26fa0-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-293">Parameters</span></span>

<span data-ttu-id="26fa0-294">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-294">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-295">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-295">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-296">aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="26fa0-296">aggregateFunction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-297">Return Value</span></span>

### <a name="method-allowqueryfilters"></a><span data-ttu-id="26fa0-298">メソッド allowQueryFilters</span><span class="sxs-lookup"><span data-stu-id="26fa0-298">Method allowQueryFilters</span></span>

    public boolean allowQueryFilters(QueryBuildDataSource dataSource)

#### <a name="parameters"></a><span data-ttu-id="26fa0-299">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-299">Parameters</span></span>

<span data-ttu-id="26fa0-300">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-300">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-301">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-301">Return Value</span></span>

### <a name="method-changedby"></a><span data-ttu-id="26fa0-302">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-302">Method changedBy</span></span>

<span data-ttu-id="26fa0-303">クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-303">Gets or sets the name of the user who last changed the Query object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-304">Parameters</span></span>

<span data-ttu-id="26fa0-305">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-305">value</span></span>  
<span data-ttu-id="26fa0-306">クエリ オブジェクトを最後に変更したユーザーの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-306">The name of the user who last changed the Query object; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-307">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-307">Return Value</span></span>

<span data-ttu-id="26fa0-308">クエリ オブジェクトを最後に変更したユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-308">The name of the user who last changed the Query object.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="26fa0-309">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-309">Method changedDate</span></span>

<span data-ttu-id="26fa0-310">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-310">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-311">Parameters</span></span>

<span data-ttu-id="26fa0-312">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-312">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-313">Return Value</span></span>

<span data-ttu-id="26fa0-314">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="26fa0-314">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="26fa0-315">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-315">Method changedTime</span></span>

<span data-ttu-id="26fa0-316">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-316">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-317">Parameters</span></span>

<span data-ttu-id="26fa0-318">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-318">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-319">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-319">Return Value</span></span>

<span data-ttu-id="26fa0-320">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="26fa0-320">The time an application object was last changed.</span></span>

### <a name="method-childdatasourcecount"></a><span data-ttu-id="26fa0-321">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-321">Method childDataSourceCount</span></span>

<span data-ttu-id="26fa0-322">クエリに関連するデータ ソースの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-322">Counts the number of data sources that are related to the query.</span></span>

    public int childDataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-323">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-323">Return Value</span></span>

<span data-ttu-id="26fa0-324">このクエリに関連するデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="26fa0-324">The number of data sources that are related to the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-325">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-325">Remarks</span></span>

<span data-ttu-id="26fa0-326">このメソッドは、トップレベルのクエリに使用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-326">This method is used for the top-level query.</span></span> <span data-ttu-id="26fa0-327">別のデータ ソースに埋め込まれているデータ ソースの数を確認するには、childDataSourceCount メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-327">To determine the number of data sources that are embedded in another data source, use the childDataSourceCount method.</span></span>

### <a name="method-childdatasourceno"></a><span data-ttu-id="26fa0-328">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-328">Method childDataSourceNo</span></span>

<span data-ttu-id="26fa0-329">指定された番号に対応するデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-329">Returns the child data source that corresponds to the specified number.</span></span>

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-330">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-330">Parameters</span></span>

<span data-ttu-id="26fa0-331">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-331">dataSourceNo</span></span>  
<span data-ttu-id="26fa0-332">子データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-332">The number of the child data source.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-333">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-333">Return Value</span></span>

<span data-ttu-id="26fa0-334">指定された番号を持つ子データ ソース。</span><span class="sxs-lookup"><span data-stu-id="26fa0-334">The child data source that has the specified number.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-335">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-335">Remarks</span></span>

<span data-ttu-id="26fa0-336">指定された数値は、クエリのすぐ下にあるデータ ソースを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-336">The number that is specified must represent a data source that is immediately underneath the query.</span></span> <span data-ttu-id="26fa0-337">通常、このようなデータ ソースは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="26fa0-337">Typically, there is only one such data source.</span></span>

### <a name="method-containsaggregatefields"></a><span data-ttu-id="26fa0-338">メソッド containsAggregateFields</span><span class="sxs-lookup"><span data-stu-id="26fa0-338">Method containsAggregateFields</span></span>

    public boolean containsAggregateFields()

#### <a name="return-value"></a><span data-ttu-id="26fa0-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-339">Return Value</span></span>

### <a name="method-createdby"></a><span data-ttu-id="26fa0-340">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-340">Method createdBy</span></span>

<span data-ttu-id="26fa0-341">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-341">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-342">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-342">Parameters</span></span>

<span data-ttu-id="26fa0-343">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-343">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-344">Return Value</span></span>

<span data-ttu-id="26fa0-345">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-345">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="26fa0-346">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-346">Method creationDate</span></span>

<span data-ttu-id="26fa0-347">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-347">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-348">Parameters</span></span>

<span data-ttu-id="26fa0-349">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-349">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-350">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-350">Return Value</span></span>

<span data-ttu-id="26fa0-351">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="26fa0-351">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="26fa0-352">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-352">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-353">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-353">Parameters</span></span>

<span data-ttu-id="26fa0-354">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-354">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-355">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-355">Return Value</span></span>

### <a name="method-datasourcecount"></a><span data-ttu-id="26fa0-356">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-356">Method dataSourceCount</span></span>

<span data-ttu-id="26fa0-357">埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-357">Returns the total number of data sources for the query, including any embedded data sources.</span></span>

    public int dataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-358">Return Value</span></span>

<span data-ttu-id="26fa0-359">このクエリのデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="26fa0-359">The number of data sources for this query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-360">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-360">Remarks</span></span>

<span data-ttu-id="26fa0-361">この番号は、データ ソースの推移的な番号であり、任意の埋め込みデータ ソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="26fa0-361">The number is the transitive number of data sources and includes any embedded data sources.</span></span>

### <a name="method-datasourcename"></a><span data-ttu-id="26fa0-362">メソッド dataSourceName</span><span class="sxs-lookup"><span data-stu-id="26fa0-362">Method dataSourceName</span></span>

<span data-ttu-id="26fa0-363">指定された名前を持つデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-363">Returns the data source that has the specified name.</span></span>

    public QueryBuildDataSource dataSourceName(str name)

#### <a name="parameters"></a><span data-ttu-id="26fa0-364">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-364">Parameters</span></span>

<span data-ttu-id="26fa0-365">名前</span><span class="sxs-lookup"><span data-stu-id="26fa0-365">name</span></span>  
<span data-ttu-id="26fa0-366">返すデータソースの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-366">The string that contains the name of the data source to return.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-367">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-367">Return Value</span></span>

<span data-ttu-id="26fa0-368">指定した名前を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="26fa0-368">The data source that has the specified name; an uninitialized object if the specified data source does not exist.</span></span>

### <a name="method-datasourceno"></a><span data-ttu-id="26fa0-369">メソッド dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-369">Method dataSourceNo</span></span>

<span data-ttu-id="26fa0-370">データ ソース番号により指定されたデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-370">Returns the data source that is specified by the data source number.</span></span>

    public QueryBuildDataSource dataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-371">Parameters</span></span>

<span data-ttu-id="26fa0-372">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-372">dataSourceNo</span></span>  
<span data-ttu-id="26fa0-373">データ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-373">The number of the data source.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-374">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-374">Return Value</span></span>

<span data-ttu-id="26fa0-375">指定した番号を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="26fa0-375">The data source that has the specified number; an uninitialized object if the specified data source does not exist.</span></span>

### <a name="method-datasourcetable"></a><span data-ttu-id="26fa0-376">メソッド dataSourceTable</span><span class="sxs-lookup"><span data-stu-id="26fa0-376">Method dataSourceTable</span></span>

<span data-ttu-id="26fa0-377">指定されたテーブルが割り当てられているデータ ソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-377">Returns the data source that the specified table is assigned to.</span></span>

    public QueryBuildDataSource dataSourceTable(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-378">Parameters</span></span>

<span data-ttu-id="26fa0-379">テーブル</span><span class="sxs-lookup"><span data-stu-id="26fa0-379">table</span></span>  
<span data-ttu-id="26fa0-380">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-380">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="26fa0-381">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-381">The default value is 1, which specifies the first (and typically only) instance.</span></span>

<!-- -->

<span data-ttu-id="26fa0-382">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-382">occurrence</span></span>  
<span data-ttu-id="26fa0-383">複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-383">An integer that is used when more than one data source uses the specified table ID; optional.</span></span> <span data-ttu-id="26fa0-384">既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-384">The default value is 1, which specifies the first (and typically only) instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-385">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-385">Return Value</span></span>

<span data-ttu-id="26fa0-386">指定されたテーブルが割り当てられているデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="26fa0-386">The data source that the specified table is assigned to.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-387">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-387">Remarks</span></span>

<span data-ttu-id="26fa0-388">データ ソースは、dataSourceNo メソッドまたは dataSourceName メソッドを呼び出すことによって取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-388">The data source can also be retrieved by calling the dataSourceNo method or the dataSourceName method.</span></span>

### <a name="method-datasourceuniqueid"></a><span data-ttu-id="26fa0-389">メソッド dataSourceUniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-389">Method dataSourceUniqueId</span></span>

    public QueryBuildDataSource dataSourceUniqueId(int uniqueId)

#### <a name="parameters"></a><span data-ttu-id="26fa0-390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-390">Parameters</span></span>

<span data-ttu-id="26fa0-391">uniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-391">uniqueId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-392">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-392">Return Value</span></span>

### <a name="method-description"></a><span data-ttu-id="26fa0-393">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-393">Method description</span></span>

    public str description([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-394">Parameters</span></span>

<span data-ttu-id="26fa0-395">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-395">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-396">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="26fa0-397">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="26fa0-397">Method equal</span></span>

<span data-ttu-id="26fa0-398">あるクエリが別のクエリと等しいかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-398">Evaluates whether one query is equal to another.</span></span>

    public boolean equal(Object record)

#### <a name="parameters"></a><span data-ttu-id="26fa0-399">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-399">Parameters</span></span>

<span data-ttu-id="26fa0-400">記録</span><span class="sxs-lookup"><span data-stu-id="26fa0-400">record</span></span>  
<span data-ttu-id="26fa0-401">比較として使用するクエリです。</span><span class="sxs-lookup"><span data-stu-id="26fa0-401">The query to use as a comparison.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-402">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-402">Return Value</span></span>

<span data-ttu-id="26fa0-403">クエリが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-403">true if the queries are equal; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-404">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-404">Remarks</span></span>

<span data-ttu-id="26fa0-405">この場合、「等しい」は、クエリが比較されるクエリと構造的に同一であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-405">"Equal" in this case means that the query is structurally identical to the query that it is compared to.</span></span> <span data-ttu-id="26fa0-406">クエリには、同じファイルに割り当てられたデータ ソースと同じ数のデータ ソースがあり、同じ数の範囲があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-406">The query has the same number of data sources assigned to the same files, and it has the same number of ranges.</span></span>

### <a name="method-exportxml"></a><span data-ttu-id="26fa0-407">メソッド exportXML</span><span class="sxs-lookup"><span data-stu-id="26fa0-407">Method exportXML</span></span>

    public str exportXML()

#### <a name="return-value"></a><span data-ttu-id="26fa0-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-408">Return Value</span></span>

### <a name="method-findhavingfilterbyfield"></a><span data-ttu-id="26fa0-409">メソッド findHavingFilterByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-409">Method findHavingFilterByField</span></span>

    public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-410">Parameters</span></span>

<span data-ttu-id="26fa0-411">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-411">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-412">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-412">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-413">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-413">occurrence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-414">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-414">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-415">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-415">Return Value</span></span>

### <a name="method-findqueryfilter"></a><span data-ttu-id="26fa0-416">メソッド findQueryFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-416">Method findQueryFilter</span></span>

    public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-417">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-417">Parameters</span></span>

<span data-ttu-id="26fa0-418">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-418">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-419">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-419">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-420">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-420">occurrence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-421">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-421">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-422">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-422">Return Value</span></span>

### <a name="method-firsttopleveldatasource"></a><span data-ttu-id="26fa0-423">メソッド firstTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-423">Method firstTopLevelDataSource</span></span>

    public QueryBuildDataSource firstTopLevelDataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-424">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-424">Return Value</span></span>

### <a name="method-forcenestedloop"></a><span data-ttu-id="26fa0-425">メソッド forceNestedLoop</span><span class="sxs-lookup"><span data-stu-id="26fa0-425">Method forceNestedLoop</span></span>

    public boolean forceNestedLoop(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="26fa0-426">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-426">Parameters</span></span>

<span data-ttu-id="26fa0-427">arg</span><span class="sxs-lookup"><span data-stu-id="26fa0-427">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-428">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-428">Return Value</span></span>

### <a name="method-forceselectorder"></a><span data-ttu-id="26fa0-429">メソッド forceSelectOrder</span><span class="sxs-lookup"><span data-stu-id="26fa0-429">Method forceSelectOrder</span></span>

    public boolean forceSelectOrder(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="26fa0-430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-430">Parameters</span></span>

<span data-ttu-id="26fa0-431">arg</span><span class="sxs-lookup"><span data-stu-id="26fa0-431">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-432">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-432">Return Value</span></span>

### <a name="method-form"></a><span data-ttu-id="26fa0-433">メソッド form</span><span class="sxs-lookup"><span data-stu-id="26fa0-433">Method form</span></span>

    public str form([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-434">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-434">Parameters</span></span>

<span data-ttu-id="26fa0-435">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-435">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-436">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-436">Return Value</span></span>

### <a name="method-getcompanyrange"></a><span data-ttu-id="26fa0-437">メソッド getCompanyRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-437">Method getCompanyRange</span></span>

    public container getCompanyRange()

#### <a name="return-value"></a><span data-ttu-id="26fa0-438">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-438">Return Value</span></span>

### <a name="method-getmostrestrictedqueryfilterstatus"></a><span data-ttu-id="26fa0-439">メソッド getMostRestrictedQueryFilterStatus</span><span class="sxs-lookup"><span data-stu-id="26fa0-439">Method getMostRestrictedQueryFilterStatus</span></span>

    public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, [int fieldId])

#### <a name="parameters"></a><span data-ttu-id="26fa0-440">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-440">Parameters</span></span>

<span data-ttu-id="26fa0-441">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-441">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-442">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-442">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-443">fieldId</span><span class="sxs-lookup"><span data-stu-id="26fa0-443">fieldId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-444">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-444">Return Value</span></span>

### <a name="method-getnextuniqueid"></a><span data-ttu-id="26fa0-445">メソッド getNextUniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-445">Method getNextUniqueId</span></span>

    public int getNextUniqueId()

#### <a name="return-value"></a><span data-ttu-id="26fa0-446">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-446">Return Value</span></span>

### <a name="method-getsqlstatement"></a><span data-ttu-id="26fa0-447">メソッド getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="26fa0-447">Method getSQLStatement</span></span>

    public str getSQLStatement([boolean noRuntimeOptimization])

#### <a name="parameters"></a><span data-ttu-id="26fa0-448">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-448">Parameters</span></span>

<span data-ttu-id="26fa0-449">noRuntimeOptimization</span><span class="sxs-lookup"><span data-stu-id="26fa0-449">noRuntimeOptimization</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-450">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-450">Return Value</span></span>

### <a name="method-getvalidtimestatedaterange"></a><span data-ttu-id="26fa0-451">メソッド getValidTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-451">Method getValidTimeStateDateRange</span></span>

    public container getValidTimeStateDateRange()

#### <a name="return-value"></a><span data-ttu-id="26fa0-452">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-452">Return Value</span></span>

### <a name="method-getvalidtimestatedatetimerange"></a><span data-ttu-id="26fa0-453">メソッド getValidTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-453">Method getValidTimeStateDateTimeRange</span></span>

    public container getValidTimeStateDateTimeRange()

#### <a name="return-value"></a><span data-ttu-id="26fa0-454">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-454">Return Value</span></span>

### <a name="method-getvalidtimestatequerytype"></a><span data-ttu-id="26fa0-455">メソッド getValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="26fa0-455">Method getValidTimeStateQueryType</span></span>

    public ValidTimeStateQueryType getValidTimeStateQueryType()

#### <a name="return-value"></a><span data-ttu-id="26fa0-456">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-456">Return Value</span></span>

### <a name="method-groupbyfield"></a><span data-ttu-id="26fa0-457">メソッド groupByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-457">Method groupByField</span></span>

    public QueryGroupByField groupByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-458">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-458">Parameters</span></span>

<span data-ttu-id="26fa0-459">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-459">index</span></span>  

<!-- -->

<span data-ttu-id="26fa0-460">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-460">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-461">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-461">Return Value</span></span>

### <a name="method-groupbyfieldcount"></a><span data-ttu-id="26fa0-462">メソッド groupByFieldCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-462">Method groupByFieldCount</span></span>

    public int groupByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-463">Parameters</span></span>

<span data-ttu-id="26fa0-464">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-464">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-465">Return Value</span></span>

### <a name="method-hasmultipletopleveldatasource"></a><span data-ttu-id="26fa0-466">メソッド hasMultipleTopLevelDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-466">Method hasMultipleTopLevelDataSource</span></span>

    public boolean hasMultipleTopLevelDataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-467">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-467">Return Value</span></span>

### <a name="method-hasrangeorfilter"></a><span data-ttu-id="26fa0-468">メソッド hasRangeOrFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-468">Method hasRangeOrFilter</span></span>

    public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)

#### <a name="parameters"></a><span data-ttu-id="26fa0-469">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-469">Parameters</span></span>

<span data-ttu-id="26fa0-470">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-470">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-471">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-471">Return Value</span></span>

### <a name="method-havingfilter"></a><span data-ttu-id="26fa0-472">メソッド havingFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-472">Method havingFilter</span></span>

    public QueryHavingFilter havingFilter(int count, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-473">Parameters</span></span>

<span data-ttu-id="26fa0-474">カウント</span><span class="sxs-lookup"><span data-stu-id="26fa0-474">count</span></span>  

<!-- -->

<span data-ttu-id="26fa0-475">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-475">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-476">Return Value</span></span>

### <a name="method-havingfiltercount"></a><span data-ttu-id="26fa0-477">メソッド havingFilterCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-477">Method havingFilterCount</span></span>

    public int havingFilterCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-478">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-478">Parameters</span></span>

<span data-ttu-id="26fa0-479">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-479">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-480">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-480">Return Value</span></span>

### <a name="method-inreport"></a><span data-ttu-id="26fa0-481">メソッド inReport</span><span class="sxs-lookup"><span data-stu-id="26fa0-481">Method inReport</span></span>

<span data-ttu-id="26fa0-482">クエリがレポートの一部であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-482">Determines whether the query is part of a report.</span></span>

    public boolean inReport()

#### <a name="return-value"></a><span data-ttu-id="26fa0-483">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-483">Return Value</span></span>

<span data-ttu-id="26fa0-484">クエリがレポートの一部である場合は (レポートのデータ ソース ノードの下にある場合は) true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-484">true if the query is part of a report (is found under a report's data sources node); otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-485">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-485">Remarks</span></span>

<span data-ttu-id="26fa0-486">この関数は、通常アプリケーション コードでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-486">This function is not typically used by application code.</span></span> <span data-ttu-id="26fa0-487">メソッドが true を返す場合は、レポート メソッドはクエリが定義されているレポートにアクセスするために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-487">If the method returns true, the report method can be used to access the report in which the query is defined.</span></span>

### <a name="method-interactive"></a><span data-ttu-id="26fa0-488">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="26fa0-488">Method interactive</span></span>

<span data-ttu-id="26fa0-489">クエリが対話的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-489">Specifies whether the query is interactive.</span></span>

    public boolean interactive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-490">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-490">Parameters</span></span>

<span data-ttu-id="26fa0-491">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-491">value</span></span>  
<span data-ttu-id="26fa0-492">クエリがインタラクティブかどうかを示す値、オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-492">A value that indicates whether the query is interactive; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-493">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-493">Return Value</span></span>

<span data-ttu-id="26fa0-494">クエリが対話形式である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-494">true if the query is interactive; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-495">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-495">Remarks</span></span>

<span data-ttu-id="26fa0-496">対話型クエリでは、たとえば prompt メソッドが呼び出されたときに、クエリはユーザーにダイアログ ボックスを提示できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-496">In an interactive query, the query can, for example, present the user with a dialog box when the prompt method is called.</span></span> <span data-ttu-id="26fa0-497">この機能は、コードをバッチに送信する場合や、コードを無人で実行する必要がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-497">This functionality is used when code will be submitted to a batch and in other situations where code must run unattended.</span></span>

### <a name="method-iscompositequery"></a><span data-ttu-id="26fa0-498">メソッド isCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-498">Method isCompositeQuery</span></span>

    public boolean isCompositeQuery()

#### <a name="return-value"></a><span data-ttu-id="26fa0-499">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-499">Return Value</span></span>

### <a name="method-isexplicitlyordered"></a><span data-ttu-id="26fa0-500">メソッド isExplicitlyOrdered</span><span class="sxs-lookup"><span data-stu-id="26fa0-500">Method isExplicitlyOrdered</span></span>

    public boolean isExplicitlyOrdered()

#### <a name="return-value"></a><span data-ttu-id="26fa0-501">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-501">Return Value</span></span>

### <a name="method-isexplicitlygrouped"></a><span data-ttu-id="26fa0-502">メソッド isExplicitlyGrouped</span><span class="sxs-lookup"><span data-stu-id="26fa0-502">Method isExplicitlyGrouped</span></span>

    public boolean isExplicitlyGrouped()

#### <a name="return-value"></a><span data-ttu-id="26fa0-503">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-503">Return Value</span></span>

### <a name="method-ispureunionall"></a><span data-ttu-id="26fa0-504">メソッド isPureUnionAll</span><span class="sxs-lookup"><span data-stu-id="26fa0-504">Method isPureUnionAll</span></span>

    public boolean isPureUnionAll()

#### <a name="return-value"></a><span data-ttu-id="26fa0-505">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-505">Return Value</span></span>

### <a name="method-isuniontype"></a><span data-ttu-id="26fa0-506">メソッド isUnionType</span><span class="sxs-lookup"><span data-stu-id="26fa0-506">Method isUnionType</span></span>

    public boolean isUnionType()

#### <a name="return-value"></a><span data-ttu-id="26fa0-507">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-507">Return Value</span></span>

### <a name="method-levelno"></a><span data-ttu-id="26fa0-508">メソッド levelNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-508">Method levelNo</span></span>

<span data-ttu-id="26fa0-509">指定されたデータ ソースのインデントのレベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-509">Determines the level of indentation of the specified data source.</span></span>

    public int levelNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-510">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-510">Parameters</span></span>

<span data-ttu-id="26fa0-511">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-511">dataSourceNo</span></span>  
<span data-ttu-id="26fa0-512">データ ソースのレベルを決定する番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-512">The data source number to determine the level for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-513">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-513">Return Value</span></span>

<span data-ttu-id="26fa0-514">指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-514">The level number of the specified data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-515">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-515">Remarks</span></span>

<span data-ttu-id="26fa0-516">データソースは、1 から順に番号付けされます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-516">The data sources are numbered consecutively, starting at 1.</span></span>

### <a name="method-leveltable"></a><span data-ttu-id="26fa0-517">メソッド levelTable</span><span class="sxs-lookup"><span data-stu-id="26fa0-517">Method levelTable</span></span>

<span data-ttu-id="26fa0-518">指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-518">Determines the tree level, in the hierarchy of data sources, of the data source that is assigned to the specified table.</span></span>

    public int levelTable(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-519">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-519">Parameters</span></span>

<span data-ttu-id="26fa0-520">テーブル</span><span class="sxs-lookup"><span data-stu-id="26fa0-520">table</span></span>  
<span data-ttu-id="26fa0-521">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-521">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

<!-- -->

<span data-ttu-id="26fa0-522">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-522">occurrence</span></span>  
<span data-ttu-id="26fa0-523">複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-523">The integer that is used if more than one data source is assigned to the same table; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-524">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-524">Return Value</span></span>

<span data-ttu-id="26fa0-525">クエリの指定されたデータ ソースのレベル番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-525">The level number of the query's specified data source.</span></span>

### <a name="method-literals"></a><span data-ttu-id="26fa0-526">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="26fa0-526">Method literals</span></span>

    public int literals([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-527">Parameters</span></span>

<span data-ttu-id="26fa0-528">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-529">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-529">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="26fa0-530">メソッド名</span><span class="sxs-lookup"><span data-stu-id="26fa0-530">Method name</span></span>

<span data-ttu-id="26fa0-531">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-531">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-532">Parameters</span></span>

<span data-ttu-id="26fa0-533">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-533">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-534">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-534">Return Value</span></span>

<span data-ttu-id="26fa0-535">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-535">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-536">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-536">Remarks</span></span>

<span data-ttu-id="26fa0-537">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-537">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="26fa0-538">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-538">Begins with a letter.</span></span>
-   <span data-ttu-id="26fa0-539">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-539">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="26fa0-540">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-540">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="26fa0-541">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-541">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="26fa0-542">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-542">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-newobject"></a><span data-ttu-id="26fa0-543">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="26fa0-543">Method newObject</span></span>

<span data-ttu-id="26fa0-544">ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-544">Creates a query that exists on the same client side or server side as the source query.</span></span>

    public Query newObject(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="26fa0-545">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-545">Parameters</span></span>

<span data-ttu-id="26fa0-546">ソース</span><span class="sxs-lookup"><span data-stu-id="26fa0-546">source</span></span>  
<span data-ttu-id="26fa0-547">ソース クエリ。</span><span class="sxs-lookup"><span data-stu-id="26fa0-547">The source query.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-548">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-548">Return Value</span></span>

<span data-ttu-id="26fa0-549">新しいクエリ。</span><span class="sxs-lookup"><span data-stu-id="26fa0-549">The new query.</span></span>

### <a name="method-nextuniqueid"></a><span data-ttu-id="26fa0-550">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-550">Method nextUniqueId</span></span>

    public int nextUniqueId([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-551">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-551">Parameters</span></span>

<span data-ttu-id="26fa0-552">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-552">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-553">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-553">Return Value</span></span>

### <a name="method-orderbyfield"></a><span data-ttu-id="26fa0-554">メソッド orderByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-554">Method orderByField</span></span>

    public QueryOrderByField orderByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-555">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-555">Parameters</span></span>

<span data-ttu-id="26fa0-556">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-556">index</span></span>  

<!-- -->

<span data-ttu-id="26fa0-557">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-557">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-558">Return Value</span></span>

### <a name="method-orderbyfieldcount"></a><span data-ttu-id="26fa0-559">メソッド orderByFieldCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-559">Method orderByFieldCount</span></span>

    public int orderByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-560">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-560">Parameters</span></span>

<span data-ttu-id="26fa0-561">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-561">dataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-562">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-562">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="26fa0-563">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="26fa0-563">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-564">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-564">Parameters</span></span>

<span data-ttu-id="26fa0-565">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-565">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-566">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-566">Return Value</span></span>

### <a name="method-pack"></a><span data-ttu-id="26fa0-567">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="26fa0-567">Method pack</span></span>

<span data-ttu-id="26fa0-568">コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-568">Packs the query into a container and returns that container, so that it can be used when you create a query.</span></span>

    public container pack([boolean doCheck])

#### <a name="parameters"></a><span data-ttu-id="26fa0-569">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-569">Parameters</span></span>

<span data-ttu-id="26fa0-570">doCheck</span><span class="sxs-lookup"><span data-stu-id="26fa0-570">doCheck</span></span>  
<span data-ttu-id="26fa0-571">クエリのデーターソースが外部のカーソルを参照する (クエリのデータソースを外部のカーソルへリンクするなど) ときに、エラーフラグを設定するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-571">A Boolean value that indicates whether to flag an error when a data source in the query references an outside cursor, such as a link to a cursor that is foreign to the query's data source; optional.</span></span> <span data-ttu-id="26fa0-572">既定値は、true で、制約が適用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-572">The default value is true, which enforces the constraint.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-573">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-573">Return Value</span></span>

<span data-ttu-id="26fa0-574">クエリを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="26fa0-574">The container that holds the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-575">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-575">Remarks</span></span>

<span data-ttu-id="26fa0-576">このメソッドで作成されたコンテナーは、新しいメソッドまたは newObject メソッドのいずれかを使用して query オブジェクトまたは queryRun オブジェクトをインスタンス化するときに入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-576">The container that is created by this method can serve as input when you instantiate a query or queryRun object by using either the new method or the newObject method.</span></span> <span data-ttu-id="26fa0-577">クエリのデータ ソースとは異なるカーソルへのリンクは、コンテナーにパックされません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-577">Links to cursors that are foreign to the query's data source are not packed into the container.</span></span> <span data-ttu-id="26fa0-578">この種類のリンクをパックする必要がある場合は、カーソルのデータのスナップショットを取得し、各フィールドの範囲を作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-578">If you must pack this kind of link, you should take a snapshot of the cursor's data and construct ranges for each field.</span></span>

### <a name="method-packinternals"></a><span data-ttu-id="26fa0-579">メソッド packInternals</span><span class="sxs-lookup"><span data-stu-id="26fa0-579">Method packInternals</span></span>

    public container packInternals()

#### <a name="return-value"></a><span data-ttu-id="26fa0-580">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-580">Return Value</span></span>

### <a name="method-queryfilter"></a><span data-ttu-id="26fa0-581">メソッド queryFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-581">Method queryFilter</span></span>

    public QueryFilter queryFilter(int count, [QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-582">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-582">Parameters</span></span>

<span data-ttu-id="26fa0-583">カウント</span><span class="sxs-lookup"><span data-stu-id="26fa0-583">count</span></span>  

<!-- -->

<span data-ttu-id="26fa0-584">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-584">rootDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-585">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-585">Return Value</span></span>

### <a name="method-queryfiltercount"></a><span data-ttu-id="26fa0-586">メソッド queryFilterCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-586">Method queryFilterCount</span></span>

    public int queryFilterCount([QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a><span data-ttu-id="26fa0-587">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-587">Parameters</span></span>

<span data-ttu-id="26fa0-588">rootDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-588">rootDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-589">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-589">Return Value</span></span>

### <a name="method-querytype"></a><span data-ttu-id="26fa0-590">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="26fa0-590">Method queryType</span></span>

    public int queryType([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-591">Parameters</span></span>

<span data-ttu-id="26fa0-592">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-592">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-593">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-593">Return Value</span></span>

### <a name="method-quickfiltervalue"></a><span data-ttu-id="26fa0-594">メソッド quickFilterValue</span><span class="sxs-lookup"><span data-stu-id="26fa0-594">Method quickFilterValue</span></span>

    public str quickFilterValue()

#### <a name="return-value"></a><span data-ttu-id="26fa0-595">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-595">Return Value</span></span>

### <a name="method-quickfiltercontrolid"></a><span data-ttu-id="26fa0-596">メソッド quickFilterControlId</span><span class="sxs-lookup"><span data-stu-id="26fa0-596">Method quickFilterControlId</span></span>

    public int quickFilterControlId()

#### <a name="return-value"></a><span data-ttu-id="26fa0-597">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-597">Return Value</span></span>

### <a name="method-recordlevelsecurity"></a><span data-ttu-id="26fa0-598">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="26fa0-598">Method recordLevelSecurity</span></span>

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-599">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-599">Parameters</span></span>

<span data-ttu-id="26fa0-600">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-600">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-601">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-601">Return Value</span></span>

### <a name="method-report"></a><span data-ttu-id="26fa0-602">メソッド report</span><span class="sxs-lookup"><span data-stu-id="26fa0-602">Method report</span></span>

<span data-ttu-id="26fa0-603">レポートが存在する場合、クエリが定義されているレポートを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-603">Returns the report in which the query is defined, if the report exists.</span></span>

    public Report report()

#### <a name="return-value"></a><span data-ttu-id="26fa0-604">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-604">Return Value</span></span>

<span data-ttu-id="26fa0-605">クエリがデータ ソース ノードの下で定義されているレポート。</span><span class="sxs-lookup"><span data-stu-id="26fa0-605">The report in which the query is defined under the data sources node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-606">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-606">Remarks</span></span>

<span data-ttu-id="26fa0-607">クエリは、必ずしもレポートのコンテキストで定義されているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-607">A query is not necessarily defined in the context of a report.</span></span> <span data-ttu-id="26fa0-608">レポートのコンテキストでクエリが定義されているかどうかを確認するには、inReport メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-608">To determine whether a query is defined in the context of a report, you can use the inReport method.</span></span>

### <a name="method-saved"></a><span data-ttu-id="26fa0-609">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="26fa0-609">Method saved</span></span>

<span data-ttu-id="26fa0-610">クエリがディスクに保存されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-610">Indicates whether the query has been saved to disk.</span></span>

    public boolean saved()

#### <a name="return-value"></a><span data-ttu-id="26fa0-611">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-611">Return Value</span></span>

<span data-ttu-id="26fa0-612">クエリがディスクに保存されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-612">true if the query has been saved to disk; otherwise, false.</span></span>

### <a name="method-searchable"></a><span data-ttu-id="26fa0-613">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="26fa0-613">Method searchable</span></span>

    public boolean searchable([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-614">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-614">Parameters</span></span>

<span data-ttu-id="26fa0-615">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-615">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-616">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-616">Return Value</span></span>

### <a name="method-importsession"></a><span data-ttu-id="26fa0-617">メソッド importSession</span><span class="sxs-lookup"><span data-stu-id="26fa0-617">Method importSession</span></span>

    public Guid importSession([Guid value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-618">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-618">Parameters</span></span>

<span data-ttu-id="26fa0-619">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-619">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-620">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-620">Return Value</span></span>

### <a name="method-title"></a><span data-ttu-id="26fa0-621">メソッド title</span><span class="sxs-lookup"><span data-stu-id="26fa0-621">Method title</span></span>

    public str title([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-622">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-622">Parameters</span></span>

<span data-ttu-id="26fa0-623">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-623">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-624">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-624">Return Value</span></span>

### <a name="method-toprows"></a><span data-ttu-id="26fa0-625">メソッド topRows</span><span class="sxs-lookup"><span data-stu-id="26fa0-625">Method topRows</span></span>

    public int topRows([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-626">Parameters</span></span>

<span data-ttu-id="26fa0-627">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-627">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-628">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-628">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-629">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-629">Method toString</span></span>

<span data-ttu-id="26fa0-630">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-630">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-631">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-631">Return Value</span></span>

<span data-ttu-id="26fa0-632">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-632">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-633">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-633">Remarks</span></span>

<span data-ttu-id="26fa0-634">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-634">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-635">ただし、メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-635">However, the method can be overridden in a derived class so that it returns values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-636">たとえば、SysMethodInfo クラスのインスタンスは、メソッド名、およびインスタンスまたは静的などのメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-636">For example, an instance of the SysMethodInfo class returns the method name, and the type of method, such as Instance or Static.</span></span>

### <a name="method-userupdate"></a><span data-ttu-id="26fa0-637">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="26fa0-637">Method userUpdate</span></span>

<span data-ttu-id="26fa0-638">フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-638">Gets or sets a value that indicates whether the query can update the records that it fetches.</span></span>

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-639">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-639">Parameters</span></span>

<span data-ttu-id="26fa0-640">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-640">value</span></span>  
<span data-ttu-id="26fa0-641">フェッチされたレコードをクエリが更新できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="26fa0-641">A Boolean value that indicates whether the query can update the records that it fetches; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-642">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-642">Return Value</span></span>

<span data-ttu-id="26fa0-643">クエリがフェッチ対象のレコードを現在更新することができる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-643">true if the query can currently update records that it fetches; otherwise false.</span></span>

### <a name="method-validtimestateasofdate"></a><span data-ttu-id="26fa0-644">メソッド validTimeStateAsOfDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-644">Method validTimeStateAsOfDate</span></span>

    public Date validTimeStateAsOfDate([Date asOfDate])

#### <a name="parameters"></a><span data-ttu-id="26fa0-645">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-645">Parameters</span></span>

<span data-ttu-id="26fa0-646">asOfDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-646">asOfDate</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-647">Return Value</span></span>

### <a name="method-validtimestateasofdatetime"></a><span data-ttu-id="26fa0-648">メソッド validTimeStateAsOfDateTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-648">Method validTimeStateAsOfDateTime</span></span>

    public DateTime validTimeStateAsOfDateTime([DateTime asOfDateTime])

#### <a name="parameters"></a><span data-ttu-id="26fa0-649">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-649">Parameters</span></span>

<span data-ttu-id="26fa0-650">asOfDateTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-650">asOfDateTime</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-651">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-651">Return Value</span></span>

### <a name="method-validtimestateflags"></a><span data-ttu-id="26fa0-652">メソッド validTimeStateFlags</span><span class="sxs-lookup"><span data-stu-id="26fa0-652">Method validTimeStateFlags</span></span>

    public int validTimeStateFlags([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-653">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-653">Parameters</span></span>

<span data-ttu-id="26fa0-654">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-654">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-655">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-655">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="26fa0-656">メソッド version</span><span class="sxs-lookup"><span data-stu-id="26fa0-656">Method version</span></span>

    public int version([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-657">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-657">Parameters</span></span>

<span data-ttu-id="26fa0-658">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-658">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-659">Return Value</span></span>

### <a name="method-xml"></a><span data-ttu-id="26fa0-660">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="26fa0-660">Method xml</span></span>

<span data-ttu-id="26fa0-661">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-661">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="26fa0-662">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-662">Parameters</span></span>

<span data-ttu-id="26fa0-663">インデント</span><span class="sxs-lookup"><span data-stu-id="26fa0-663">indent</span></span>  
<span data-ttu-id="26fa0-664">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-664">The amount of indentation for the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-665">Return Value</span></span>

<span data-ttu-id="26fa0-666">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="26fa0-666">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-667">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-667">Remarks</span></span>

<span data-ttu-id="26fa0-668">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-668">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-clearbasequeries"></a><span data-ttu-id="26fa0-669">メソッド clearBaseQueries</span><span class="sxs-lookup"><span data-stu-id="26fa0-669">Method clearBaseQueries</span></span>

    public void clearBaseQueries()

### <a name="method-addcompanyrange"></a><span data-ttu-id="26fa0-670">メソッド addCompanyRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-670">Method addCompanyRange</span></span>

    public void addCompanyRange(str companyName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-671">Parameters</span></span>

<span data-ttu-id="26fa0-672">companyName</span><span class="sxs-lookup"><span data-stu-id="26fa0-672">companyName</span></span>  

### <a name="method-checkrangeparsingerrors"></a><span data-ttu-id="26fa0-673">メソッド checkRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="26fa0-673">Method checkRangeParsingErrors</span></span>

    public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)

#### <a name="parameters"></a><span data-ttu-id="26fa0-674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-674">Parameters</span></span>

<span data-ttu-id="26fa0-675">setCheckRangeParsingErrors</span><span class="sxs-lookup"><span data-stu-id="26fa0-675">setCheckRangeParsingErrors</span></span>  

### <a name="method-clearcompanyrange"></a><span data-ttu-id="26fa0-676">メソッド clearCompanyRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-676">Method clearCompanyRange</span></span>

    public void clearCompanyRange()

### <a name="method-unpackinternals"></a><span data-ttu-id="26fa0-677">メソッド unpackInternals</span><span class="sxs-lookup"><span data-stu-id="26fa0-677">Method unpackInternals</span></span>

    public void unpackInternals(container internalData)

#### <a name="parameters"></a><span data-ttu-id="26fa0-678">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-678">Parameters</span></span>

<span data-ttu-id="26fa0-679">internalData</span><span class="sxs-lookup"><span data-stu-id="26fa0-679">internalData</span></span>  

### <a name="method-new"></a><span data-ttu-id="26fa0-680">メソッド new</span><span class="sxs-lookup"><span data-stu-id="26fa0-680">Method new</span></span>

<span data-ttu-id="26fa0-681">クエリ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-681">Creates a query object.</span></span>

    public void new([AnyType source])

#### <a name="parameters"></a><span data-ttu-id="26fa0-682">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-682">Parameters</span></span>

<span data-ttu-id="26fa0-683">ソース</span><span class="sxs-lookup"><span data-stu-id="26fa0-683">source</span></span>  
<span data-ttu-id="26fa0-684">クエリ オブジェクトを基にするソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-684">The source to base the query object on; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-685">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-685">Remarks</span></span>

<span data-ttu-id="26fa0-686">このメソッドが呼び出されときに引数を指定すると、将来使用するために、Finance and Operations アプリケーション オブジェクト ツリー (AOT) で保存されていない一時的なクエリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-686">If no arguments are supplied when this method is called, a temporary query is created that is not stored in the Finance and Operations Application Object Tree (AOT) for subsequent use.</span></span>

### <a name="method-checkfieldaccess"></a><span data-ttu-id="26fa0-687">メソッド checkFieldAccess</span><span class="sxs-lookup"><span data-stu-id="26fa0-687">Method checkFieldAccess</span></span>

    public void checkFieldAccess(boolean setCheckFieldAccess)

#### <a name="parameters"></a><span data-ttu-id="26fa0-688">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-688">Parameters</span></span>

<span data-ttu-id="26fa0-689">setCheckFieldAccess</span><span class="sxs-lookup"><span data-stu-id="26fa0-689">setCheckFieldAccess</span></span>  

### <a name="method-usedbcacheongeneratedcursors"></a><span data-ttu-id="26fa0-690">メソッド useDbCacheOnGeneratedCursors</span><span class="sxs-lookup"><span data-stu-id="26fa0-690">Method useDbCacheOnGeneratedCursors</span></span>

    public void useDbCacheOnGeneratedCursors([int fetchsize])

#### <a name="parameters"></a><span data-ttu-id="26fa0-691">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-691">Parameters</span></span>

<span data-ttu-id="26fa0-692">fetchsize</span><span class="sxs-lookup"><span data-stu-id="26fa0-692">fetchsize</span></span>  

### <a name="method-setvalidtimestatequerytype"></a><span data-ttu-id="26fa0-693">メソッド setValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="26fa0-693">Method setValidTimeStateQueryType</span></span>

    public void setValidTimeStateQueryType([ValidTimeStateQueryType type])

#### <a name="parameters"></a><span data-ttu-id="26fa0-694">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-694">Parameters</span></span>

<span data-ttu-id="26fa0-695">タイプ</span><span class="sxs-lookup"><span data-stu-id="26fa0-695">type</span></span>  

### <a name="method-validtimestatedaterange"></a><span data-ttu-id="26fa0-696">メソッド validTimeStateDateRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-696">Method validTimeStateDateRange</span></span>

    public void validTimeStateDateRange([Date fromDate], [Date toDate])

#### <a name="parameters"></a><span data-ttu-id="26fa0-697">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-697">Parameters</span></span>

<span data-ttu-id="26fa0-698">fromDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-698">fromDate</span></span>  

<!-- -->

<span data-ttu-id="26fa0-699">toDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-699">toDate</span></span>  

### <a name="method-clearhavingfilters"></a><span data-ttu-id="26fa0-700">メソッド clearHavingFilters</span><span class="sxs-lookup"><span data-stu-id="26fa0-700">Method clearHavingFilters</span></span>

    public void clearHavingFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-701">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-701">Parameters</span></span>

<span data-ttu-id="26fa0-702">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-702">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-703">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-703">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-704">occurence</span><span class="sxs-lookup"><span data-stu-id="26fa0-704">occurence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-705">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-705">arrayIndex</span></span>  

### <a name="method-quickfilter"></a><span data-ttu-id="26fa0-706">メソッド quickFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-706">Method quickFilter</span></span>

    public void quickFilter([str dataSourceName], [int tableId], [int fieldId], [str filterValue], [int controlId], [boolean useEqualityComparisonForStrings])

#### <a name="parameters"></a><span data-ttu-id="26fa0-707">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-707">Parameters</span></span>

<span data-ttu-id="26fa0-708">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="26fa0-708">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-709">tableId</span><span class="sxs-lookup"><span data-stu-id="26fa0-709">tableId</span></span>  

<!-- -->

<span data-ttu-id="26fa0-710">fieldId</span><span class="sxs-lookup"><span data-stu-id="26fa0-710">fieldId</span></span>  

<!-- -->

<span data-ttu-id="26fa0-711">filterValue</span><span class="sxs-lookup"><span data-stu-id="26fa0-711">filterValue</span></span>  

<!-- -->

<span data-ttu-id="26fa0-712">controlId</span><span class="sxs-lookup"><span data-stu-id="26fa0-712">controlId</span></span>  

<!-- -->

<span data-ttu-id="26fa0-713">useEqualityComparisonForStrings</span><span class="sxs-lookup"><span data-stu-id="26fa0-713">useEqualityComparisonForStrings</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="26fa0-714">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-714">Method finalize</span></span>

    public void finalize()

### <a name="method-clearqueryfilters"></a><span data-ttu-id="26fa0-715">メソッド clearQueryFilters</span><span class="sxs-lookup"><span data-stu-id="26fa0-715">Method clearQueryFilters</span></span>

    public void clearQueryFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-716">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-716">Parameters</span></span>

<span data-ttu-id="26fa0-717">dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-717">dataSource</span></span>  

<!-- -->

<span data-ttu-id="26fa0-718">fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-718">fieldName</span></span>  

<!-- -->

<span data-ttu-id="26fa0-719">occurence</span><span class="sxs-lookup"><span data-stu-id="26fa0-719">occurence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-720">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-720">arrayIndex</span></span>  

### <a name="method-clearorderby"></a><span data-ttu-id="26fa0-721">メソッド clearOrderBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-721">Method clearOrderBy</span></span>

    public void clearOrderBy()

### <a name="method-clearallfields"></a><span data-ttu-id="26fa0-722">メソッド clearAllFields</span><span class="sxs-lookup"><span data-stu-id="26fa0-722">Method clearAllFields</span></span>

    public void clearAllFields()

### <a name="method-cleargroupby"></a><span data-ttu-id="26fa0-723">メソッド clearGroupBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-723">Method clearGroupBy</span></span>

    public void clearGroupBy()

### <a name="method-autoauthzmode"></a><span data-ttu-id="26fa0-724">メソッド autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="26fa0-724">Method autoAuthzMode</span></span>

    public void autoAuthzMode(AutoAuthzMode mode)

#### <a name="parameters"></a><span data-ttu-id="26fa0-725">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-725">Parameters</span></span>

<span data-ttu-id="26fa0-726">モード</span><span class="sxs-lookup"><span data-stu-id="26fa0-726">mode</span></span>  

### <a name="method-insert_recordset"></a><span data-ttu-id="26fa0-727">メソッド insert\_recordset</span><span class="sxs-lookup"><span data-stu-id="26fa0-727">Method insert\_recordset</span></span>

    public static void insert_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)

#### <a name="parameters"></a><span data-ttu-id="26fa0-728">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-728">Parameters</span></span>

<span data-ttu-id="26fa0-729">targetCursor</span><span class="sxs-lookup"><span data-stu-id="26fa0-729">targetCursor</span></span>  

<!-- -->

<span data-ttu-id="26fa0-730">targetToSourceMap</span><span class="sxs-lookup"><span data-stu-id="26fa0-730">targetToSourceMap</span></span>  

<!-- -->

<span data-ttu-id="26fa0-731">sourceQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-731">sourceQuery</span></span>  

### <a name="method-generatecursors"></a><span data-ttu-id="26fa0-732">メソッド generateCursors</span><span class="sxs-lookup"><span data-stu-id="26fa0-732">Method generateCursors</span></span>

    public void generateCursors()

### <a name="method-checkauthorizationonopenranges"></a><span data-ttu-id="26fa0-733">メソッド checkAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="26fa0-733">Method checkAuthorizationOnOpenRanges</span></span>

    public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)

#### <a name="parameters"></a><span data-ttu-id="26fa0-734">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-734">Parameters</span></span>

<span data-ttu-id="26fa0-735">setCheckAuthorizationOnOpenRanges</span><span class="sxs-lookup"><span data-stu-id="26fa0-735">setCheckAuthorizationOnOpenRanges</span></span>  

### <a name="method-addcontains"></a><span data-ttu-id="26fa0-736">メソッド addContains</span><span class="sxs-lookup"><span data-stu-id="26fa0-736">Method addContains</span></span>

    public void addContains(str containsValue, [boolean prefixSearch])

#### <a name="parameters"></a><span data-ttu-id="26fa0-737">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-737">Parameters</span></span>

<span data-ttu-id="26fa0-738">containsValue</span><span class="sxs-lookup"><span data-stu-id="26fa0-738">containsValue</span></span>  

<!-- -->

<span data-ttu-id="26fa0-739">prefixSearch</span><span class="sxs-lookup"><span data-stu-id="26fa0-739">prefixSearch</span></span>  

### <a name="method-resetvalidtimestatequerytype"></a><span data-ttu-id="26fa0-740">メソッド resetValidTimeStateQueryType</span><span class="sxs-lookup"><span data-stu-id="26fa0-740">Method resetValidTimeStateQueryType</span></span>

    public void resetValidTimeStateQueryType()

### <a name="method-validtimestatedatetimerange"></a><span data-ttu-id="26fa0-741">メソッド validTimeStateDateTimeRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-741">Method validTimeStateDateTimeRange</span></span>

    public void validTimeStateDateTimeRange([DateTime fromDateTime], [DateTime toDateTime])

#### <a name="parameters"></a><span data-ttu-id="26fa0-742">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-742">Parameters</span></span>

<span data-ttu-id="26fa0-743">fromDateTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-743">fromDateTime</span></span>  

<!-- -->

<span data-ttu-id="26fa0-744">toDateTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-744">toDateTime</span></span>  

## <a name="class-querybuilddatasource"></a><span data-ttu-id="26fa0-745">クラス QueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-745">Class QueryBuildDataSource</span></span>
    class QueryBuildDataSource extends TreeNode

<span data-ttu-id="26fa0-746">QueryBuildDataSource クラスは、クエリが構成されているレポート パーツを提供します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-746">The QueryBuildDataSource class provides the building blocks that queries are made of.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-747">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-747">Remarks</span></span>

<span data-ttu-id="26fa0-748">データ ソースは、データ ソースに割り当てられたテーブルからレコードがフェッチされる順序を定義する階層内で配置されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-748">Data sources are arranged in hierarchies that define the sequence in which records are fetched from the tables that are assigned to the data sources.</span></span> <span data-ttu-id="26fa0-749">各データ ソースでは、レコードがフェッチされる順序および選択されたレコードによって満たされなければならない基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-749">Each data source defines the order in which the records are fetched, and also the criteria that must be met by the selected records.</span></span> <span data-ttu-id="26fa0-750">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-750">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="26fa0-751">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-751">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-752">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-752">Examples</span></span>

    {    QueryBuildDataSource ds;    Query q = new Query();        ds = q.addDataSource(        TableNum(CustTable));}

### <a name="methods"></a><span data-ttu-id="26fa0-753">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-753">Methods</span></span>

| <span data-ttu-id="26fa0-754">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-754">Method</span></span>                                                                                                                                                       | <span data-ttu-id="26fa0-755">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-755">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fa0-756">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-756">public int addAllFields(TableName tableName)</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-757">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-757">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span></span>                                                             | <span data-ttu-id="26fa0-758">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-758">Adds a data source that is embedded in this data source.</span></span>                                                                                  |
| <span data-ttu-id="26fa0-759">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-759">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span></span>      |                                                                                                                                           |
| <span data-ttu-id="26fa0-760">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-760">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-761">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-761">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-762">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-762">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-763">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-763">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-764">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-764">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-765">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-765">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-766">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-766">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span></span>                                                             | <span data-ttu-id="26fa0-767">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-767">Adds a range to the data source.</span></span>                                                                                                          |
| <span data-ttu-id="26fa0-768">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-768">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-769">public int addSortIndex(IndexId index)</span><span class="sxs-lookup"><span data-stu-id="26fa0-769">public int addSortIndex(IndexId index)</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-770">public int allowAdd(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-770">public int allowAdd(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-771">public boolean applyFilter(FilterValue filterValue)</span><span class="sxs-lookup"><span data-stu-id="26fa0-771">public boolean applyFilter(FilterValue filterValue)</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-772">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-772">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-773">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-773">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-774">public boolean autoSum(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-774">public boolean autoSum(FieldId field, \[boolean orderNo\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-775">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-775">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-776">public boolean changedNo()</span><span class="sxs-lookup"><span data-stu-id="26fa0-776">public boolean changedNo()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-777">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-777">public int childDataSourceCount()</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-778">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-778">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-779">public str company(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-779">public str company(\[str value\])</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-780">public int concurrencyModel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-780">public int concurrencyModel(\[int value\])</span></span>                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-781">public QueryBuildDynalink dynalink(int dynalinkNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-781">public QueryBuildDynalink dynalink(int dynalinkNo)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-782">public int dynalinkCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-782">public int dynalinkCount()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-783">public boolean embedded()</span><span class="sxs-lookup"><span data-stu-id="26fa0-783">public boolean embedded()</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-784">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-784">public boolean enabled(\[boolean value\])</span></span>                                                                                                                    | <span data-ttu-id="26fa0-785">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-785">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="26fa0-786">public boolean existsMeanOrExists(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-786">public boolean existsMeanOrExists(\[boolean value\])</span></span>                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-787">public int fetchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-787">public int fetchMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-788">public QueryBuildFieldList fields()</span><span class="sxs-lookup"><span data-stu-id="26fa0-788">public QueryBuildFieldList fields()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-789">public TableId file()</span><span class="sxs-lookup"><span data-stu-id="26fa0-789">public TableId file()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-790">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-790">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-791">public boolean firstFast(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-791">public boolean firstFast(\[boolean value\])</span></span>                                                                                                                  | <span data-ttu-id="26fa0-792">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-792">Determines whether to retrieve the first record from the query before the other records.</span></span>                                                  |
| <span data-ttu-id="26fa0-793">public boolean firstOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-793">public boolean firstOnly(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-794">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-794">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-795">public Common getNo()</span><span class="sxs-lookup"><span data-stu-id="26fa0-795">public Common getNo()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-796">public int id()</span><span class="sxs-lookup"><span data-stu-id="26fa0-796">public int id()</span></span>                                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-797">public boolean indexIsHint(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="26fa0-797">public boolean indexIsHint(boolean arg)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-798">public boolean isPartOfSubQueryInBaseQuery()</span><span class="sxs-lookup"><span data-stu-id="26fa0-798">public boolean isPartOfSubQueryInBaseQuery()</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-799">public boolean joined()</span><span class="sxs-lookup"><span data-stu-id="26fa0-799">public boolean joined()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-800">public container joinedDataSources()</span><span class="sxs-lookup"><span data-stu-id="26fa0-800">public container joinedDataSources()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-801">public int joinMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-801">public int joinMode(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-802">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-802">public str label(\[str value\])</span></span>                                                                                                                              | <span data-ttu-id="26fa0-803">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-803">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="26fa0-804">public int level()</span><span class="sxs-lookup"><span data-stu-id="26fa0-804">public int level()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-805">public QueryBuildLink link(int associationNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-805">public QueryBuildLink link(int associationNo)</span></span>                                                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-806">public int linkCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-806">public int linkCount()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-807">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-807">public str name(\[str value\])</span></span>                                                                                                                               | <span data-ttu-id="26fa0-808">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-808">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="26fa0-809">public container oneToOneDataSources()</span><span class="sxs-lookup"><span data-stu-id="26fa0-809">public container oneToOneDataSources()</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-810">public int orderMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-810">public int orderMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-811">public QueryBuildDataSource parentDataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-811">public QueryBuildDataSource parentDataSource()</span></span>                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-812">public str policyContext(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-812">public str policyContext(\[str value\])</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-813">public QueryBuildRange range(int rangeNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-813">public QueryBuildRange range(int rangeNo)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-814">public int rangeCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-814">public int rangeCount()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-815">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-815">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-816">public boolean relations(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-816">public boolean relations(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-817">public int selectionCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-817">public int selectionCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-818">public boolean selectWithRepeatableRead(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-818">public boolean selectWithRepeatableRead(\[boolean value\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-819">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-819">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-820">public FieldId sortField(FieldId field)</span><span class="sxs-lookup"><span data-stu-id="26fa0-820">public FieldId sortField(FieldId field)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-821">public int sortFieldCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-821">public int sortFieldCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-822">public IndexId sortIndex(int indexNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-822">public IndexId sortIndex(int indexNo)</span></span>                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-823">public int sortIndexCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-823">public int sortIndexCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-824">public QueryBuildStaticlink staticlink(int staticlinkNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-824">public QueryBuildStaticlink staticlink(int staticlinkNo)</span></span>                                                                                                     | <span data-ttu-id="26fa0-825">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-825">Returns a static Link object on the query’s data source.</span></span>                                                                                  |
| <span data-ttu-id="26fa0-826">public int staticlinkCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-826">public int staticlinkCount()</span></span>                                                                                                                                 | <span data-ttu-id="26fa0-827">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-827">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>                                                     |
| <span data-ttu-id="26fa0-828">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-828">public TableId table(\[TableId value\])</span></span>                                                                                                                      | <span data-ttu-id="26fa0-829">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-829">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="26fa0-830">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-830">public str toString()</span></span>                                                                                                                                        | <span data-ttu-id="26fa0-831">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-831">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-832">public int unionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-832">public int unionType(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-833">public int uniqueId()</span><span class="sxs-lookup"><span data-stu-id="26fa0-833">public int uniqueId()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-834">public boolean update(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-834">public boolean update(\[boolean value\])</span></span>                                                                                                                     | <span data-ttu-id="26fa0-835">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-835">Determines whether the records fetched by this data source can be updated.</span></span>                                                                |
| <span data-ttu-id="26fa0-836">public void clearLinks()</span><span class="sxs-lookup"><span data-stu-id="26fa0-836">public void clearLinks()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-837">public void clearDynalinks()</span><span class="sxs-lookup"><span data-stu-id="26fa0-837">public void clearDynalinks()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-838">public void clearRange(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-838">public void clearRange(FieldId field, \[int occurrence\])</span></span>                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-839">public void sortClear()</span><span class="sxs-lookup"><span data-stu-id="26fa0-839">public void sortClear()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-840">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-840">public void finalize()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-841">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-841">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-842">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span><span class="sxs-lookup"><span data-stu-id="26fa0-842">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-843">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span><span class="sxs-lookup"><span data-stu-id="26fa0-843">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-844">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-844">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-845">public void clearSortIndex()</span><span class="sxs-lookup"><span data-stu-id="26fa0-845">public void clearSortIndex()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-846">public void clearRanges()</span><span class="sxs-lookup"><span data-stu-id="26fa0-846">public void clearRanges()</span></span>                                                                                                                                    | <span data-ttu-id="26fa0-847">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-847">Deletes all ranges that are associated with the data source.</span></span>                                                                              |
| <span data-ttu-id="26fa0-848">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-848">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-849">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-849">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span></span>                                                               |                                                                                                                                           |

### <a name="method-addallfields"></a><span data-ttu-id="26fa0-850">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="26fa0-850">Method addAllFields</span></span>

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-851">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-851">Parameters</span></span>

<span data-ttu-id="26fa0-852">tableName</span><span class="sxs-lookup"><span data-stu-id="26fa0-852">tableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-853">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-853">Return Value</span></span>

### <a name="method-adddatasource"></a><span data-ttu-id="26fa0-854">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-854">Method addDataSource</span></span>

<span data-ttu-id="26fa0-855">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-855">Adds a data source that is embedded in this data source.</span></span>

    public QueryBuildDataSource addDataSource(AnyType arg, [str name], [boolean emptyFieldList])

#### <a name="parameters"></a><span data-ttu-id="26fa0-856">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-856">Parameters</span></span>

<span data-ttu-id="26fa0-857">arg</span><span class="sxs-lookup"><span data-stu-id="26fa0-857">arg</span></span>  

<!-- -->

<span data-ttu-id="26fa0-858">名前</span><span class="sxs-lookup"><span data-stu-id="26fa0-858">name</span></span>  

<!-- -->

<span data-ttu-id="26fa0-859">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="26fa0-859">emptyFieldList</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-860">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-860">Return Value</span></span>

<span data-ttu-id="26fa0-861">新しいデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-861">The new data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-862">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-862">Remarks</span></span>

<span data-ttu-id="26fa0-863">最上位レベルのデータ ソースは、addDataSource メソッドを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-863">Top-level data sources are created by using the addDataSource method.</span></span>

### <a name="method-adddynalink"></a><span data-ttu-id="26fa0-864">メソッド addDynalink</span><span class="sxs-lookup"><span data-stu-id="26fa0-864">Method addDynalink</span></span>

    public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, [int fieldArrayIndex], [int dynamicFieldArrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-865">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-865">Parameters</span></span>

<span data-ttu-id="26fa0-866">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-866">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-867">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="26fa0-867">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="26fa0-868">dynamicField</span><span class="sxs-lookup"><span data-stu-id="26fa0-868">dynamicField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-869">fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-869">fieldArrayIndex</span></span>  

<!-- -->

<span data-ttu-id="26fa0-870">dynamicFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-870">dynamicFieldArrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-871">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-871">Return Value</span></span>

### <a name="method-addforeignkeyrelation"></a><span data-ttu-id="26fa0-872">メソッド addForeignkeyRelation</span><span class="sxs-lookup"><span data-stu-id="26fa0-872">Method addForeignkeyRelation</span></span>

    public QueryBuildLink addForeignkeyRelation(str relatedTableRole, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="26fa0-873">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-873">Parameters</span></span>

<span data-ttu-id="26fa0-874">relatedTableRole</span><span class="sxs-lookup"><span data-stu-id="26fa0-874">relatedTableRole</span></span>  

<!-- -->

<span data-ttu-id="26fa0-875">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="26fa0-875">parentDatasourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-876">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-876">Return Value</span></span>

### <a name="method-addgroupbyfield"></a><span data-ttu-id="26fa0-877">メソッド addGroupByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-877">Method addGroupByField</span></span>

    public QueryGroupByField addGroupByField(FieldId fieldID, [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-878">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-878">Parameters</span></span>

<span data-ttu-id="26fa0-879">fieldID</span><span class="sxs-lookup"><span data-stu-id="26fa0-879">fieldID</span></span>  

<!-- -->

<span data-ttu-id="26fa0-880">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-880">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-881">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-881">Return Value</span></span>

### <a name="method-addlink"></a><span data-ttu-id="26fa0-882">メソッド addLink</span><span class="sxs-lookup"><span data-stu-id="26fa0-882">Method addLink</span></span>

    public QueryBuildLink addLink(FieldId parentField, FieldId thisField, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="26fa0-883">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-883">Parameters</span></span>

<span data-ttu-id="26fa0-884">parentField</span><span class="sxs-lookup"><span data-stu-id="26fa0-884">parentField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-885">thisField</span><span class="sxs-lookup"><span data-stu-id="26fa0-885">thisField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-886">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="26fa0-886">parentDatasourceName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-887">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-887">Return Value</span></span>

### <a name="method-addorderbyaggregatefield"></a><span data-ttu-id="26fa0-888">メソッド addOrderByAggregateField</span><span class="sxs-lookup"><span data-stu-id="26fa0-888">Method addOrderByAggregateField</span></span>

    public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-889">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-889">Parameters</span></span>

<span data-ttu-id="26fa0-890">fieldType</span><span class="sxs-lookup"><span data-stu-id="26fa0-890">fieldType</span></span>  

<!-- -->

<span data-ttu-id="26fa0-891">fieldID</span><span class="sxs-lookup"><span data-stu-id="26fa0-891">fieldID</span></span>  

<!-- -->

<span data-ttu-id="26fa0-892">direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-892">direction</span></span>  

<!-- -->

<span data-ttu-id="26fa0-893">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-893">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-894">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-894">Return Value</span></span>

### <a name="method-addorderbycalculationfield"></a><span data-ttu-id="26fa0-895">メソッド addOrderByCalculationField</span><span class="sxs-lookup"><span data-stu-id="26fa0-895">Method addOrderByCalculationField</span></span>

    public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, [SortOrder direction])

#### <a name="parameters"></a><span data-ttu-id="26fa0-896">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-896">Parameters</span></span>

<span data-ttu-id="26fa0-897">計算</span><span class="sxs-lookup"><span data-stu-id="26fa0-897">calculation</span></span>  

<!-- -->

<span data-ttu-id="26fa0-898">direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-898">direction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-899">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-899">Return Value</span></span>

### <a name="method-addorderbyfield"></a><span data-ttu-id="26fa0-900">メソッド addOrderByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-900">Method addOrderByField</span></span>

    public QueryOrderByField addOrderByField(FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-901">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-901">Parameters</span></span>

<span data-ttu-id="26fa0-902">fieldID</span><span class="sxs-lookup"><span data-stu-id="26fa0-902">fieldID</span></span>  

<!-- -->

<span data-ttu-id="26fa0-903">direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-903">direction</span></span>  

<!-- -->

<span data-ttu-id="26fa0-904">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-904">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-905">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-905">Return Value</span></span>

### <a name="method-addrange"></a><span data-ttu-id="26fa0-906">メソッド addRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-906">Method addRange</span></span>

<span data-ttu-id="26fa0-907">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-907">Adds a range to the data source.</span></span>

    public QueryBuildRange addRange(FieldId field, [int arrayIndex], [QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="26fa0-908">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-908">Parameters</span></span>

<span data-ttu-id="26fa0-909">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-909">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-910">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-910">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="26fa0-911">rangeType</span><span class="sxs-lookup"><span data-stu-id="26fa0-911">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-912">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-912">Return Value</span></span>

<span data-ttu-id="26fa0-913">データ ソースの新しい範囲。</span><span class="sxs-lookup"><span data-stu-id="26fa0-913">A new range for the data source.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-914">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-914">Remarks</span></span>

<span data-ttu-id="26fa0-915">範囲は、データ ソースのテーブルのレコードが満たす必要がある値を定義します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-915">Ranges define the values that records from the data source's table must satisfy.</span></span> <span data-ttu-id="26fa0-916">いくつかの値の範囲は、特定のデータ ソース内の同じフィールドに存在することができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-916">Several range values can exist for the same field in a particular data source.</span></span> <span data-ttu-id="26fa0-917">この場合、レコードが提供される値のいずれかにが適用される場合、値はクエリに含まれます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-917">In this case, the values are included in the query if the record qualifies for any of the values that are supplied.</span></span> <span data-ttu-id="26fa0-918">複数のフィールドの範囲が含まれているときは、両方の条件によって提供される制約を満たすレコードだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-918">When ranges are included for multiple fields, only records that satisfy the constraints that are supplied by both criteria are included.</span></span> <span data-ttu-id="26fa0-919">制約は値のメソッドで指定されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-919">The constraints are specified in the value method.</span></span>

### <a name="method-addsortfield"></a><span data-ttu-id="26fa0-920">メソッド addSortField</span><span class="sxs-lookup"><span data-stu-id="26fa0-920">Method addSortField</span></span>

    public int addSortField(FieldId sortField, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-921">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-921">Parameters</span></span>

<span data-ttu-id="26fa0-922">sortField</span><span class="sxs-lookup"><span data-stu-id="26fa0-922">sortField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-923">direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-923">direction</span></span>  

<!-- -->

<span data-ttu-id="26fa0-924">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-924">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-925">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-925">Return Value</span></span>

### <a name="method-addsortindex"></a><span data-ttu-id="26fa0-926">メソッド addSortIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-926">Method addSortIndex</span></span>

    public int addSortIndex(IndexId index)

#### <a name="parameters"></a><span data-ttu-id="26fa0-927">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-927">Parameters</span></span>

<span data-ttu-id="26fa0-928">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-928">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-929">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-929">Return Value</span></span>

### <a name="method-allowadd"></a><span data-ttu-id="26fa0-930">メソッド allowAdd</span><span class="sxs-lookup"><span data-stu-id="26fa0-930">Method allowAdd</span></span>

    public int allowAdd([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-931">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-931">Parameters</span></span>

<span data-ttu-id="26fa0-932">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-932">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-933">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-933">Return Value</span></span>

### <a name="method-applyfilter"></a><span data-ttu-id="26fa0-934">メソッド applyFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-934">Method applyFilter</span></span>

    public boolean applyFilter(FilterValue filterValue)

#### <a name="parameters"></a><span data-ttu-id="26fa0-935">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-935">Parameters</span></span>

<span data-ttu-id="26fa0-936">filterValue</span><span class="sxs-lookup"><span data-stu-id="26fa0-936">filterValue</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-937">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-937">Return Value</span></span>

### <a name="method-autoheader"></a><span data-ttu-id="26fa0-938">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="26fa0-938">Method autoHeader</span></span>

    public boolean autoHeader(FieldId field, [boolean orderNo])

#### <a name="parameters"></a><span data-ttu-id="26fa0-939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-939">Parameters</span></span>

<span data-ttu-id="26fa0-940">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-940">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-941">orderNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-941">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-942">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-942">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="26fa0-943">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-943">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a><span data-ttu-id="26fa0-944">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-944">Parameters</span></span>

<span data-ttu-id="26fa0-945">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-945">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-946">orderNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-946">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-947">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-947">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="26fa0-948">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="26fa0-948">Method autoSum</span></span>

    public boolean autoSum(FieldId field, [boolean orderNo])

#### <a name="parameters"></a><span data-ttu-id="26fa0-949">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-949">Parameters</span></span>

<span data-ttu-id="26fa0-950">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-950">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-951">orderNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-951">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-952">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-952">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="26fa0-953">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-953">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a><span data-ttu-id="26fa0-954">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-954">Parameters</span></span>

<span data-ttu-id="26fa0-955">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-955">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-956">orderNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-956">orderNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-957">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-957">Return Value</span></span>

### <a name="method-changedno"></a><span data-ttu-id="26fa0-958">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-958">Method changedNo</span></span>

    public boolean changedNo()

#### <a name="return-value"></a><span data-ttu-id="26fa0-959">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-959">Return Value</span></span>

### <a name="method-childdatasourcecount"></a><span data-ttu-id="26fa0-960">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-960">Method childDataSourceCount</span></span>

    public int childDataSourceCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-961">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-961">Return Value</span></span>

### <a name="method-childdatasourceno"></a><span data-ttu-id="26fa0-962">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-962">Method childDataSourceNo</span></span>

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-963">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-963">Parameters</span></span>

<span data-ttu-id="26fa0-964">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-964">dataSourceNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-965">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-965">Return Value</span></span>

### <a name="method-company"></a><span data-ttu-id="26fa0-966">メソッド company</span><span class="sxs-lookup"><span data-stu-id="26fa0-966">Method company</span></span>

    public str company([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-967">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-967">Parameters</span></span>

<span data-ttu-id="26fa0-968">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-968">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-969">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-969">Return Value</span></span>

### <a name="method-concurrencymodel"></a><span data-ttu-id="26fa0-970">メソッド concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="26fa0-970">Method concurrencyModel</span></span>

    public int concurrencyModel([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-971">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-971">Parameters</span></span>

<span data-ttu-id="26fa0-972">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-972">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-973">Return Value</span></span>

### <a name="method-dynalink"></a><span data-ttu-id="26fa0-974">メソッド dynalink</span><span class="sxs-lookup"><span data-stu-id="26fa0-974">Method dynalink</span></span>

    public QueryBuildDynalink dynalink(int dynalinkNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-975">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-975">Parameters</span></span>

<span data-ttu-id="26fa0-976">dynalinkNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-976">dynalinkNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-977">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-977">Return Value</span></span>

### <a name="method-dynalinkcount"></a><span data-ttu-id="26fa0-978">メソッド dynalinkCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-978">Method dynalinkCount</span></span>

    public int dynalinkCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-979">Return Value</span></span>

### <a name="method-embedded"></a><span data-ttu-id="26fa0-980">メソッド embedded</span><span class="sxs-lookup"><span data-stu-id="26fa0-980">Method embedded</span></span>

    public boolean embedded()

#### <a name="return-value"></a><span data-ttu-id="26fa0-981">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-981">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="26fa0-982">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="26fa0-982">Method enabled</span></span>

<span data-ttu-id="26fa0-983">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-983">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-984">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-984">Parameters</span></span>

<span data-ttu-id="26fa0-985">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-985">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-986">Return Value</span></span>

<span data-ttu-id="26fa0-987">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-987">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-988">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-988">Remarks</span></span>

<span data-ttu-id="26fa0-989">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-989">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="26fa0-990">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-990">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="26fa0-991">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-991">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-existsmeanorexists"></a><span data-ttu-id="26fa0-992">メソッド existsMeanOrExists</span><span class="sxs-lookup"><span data-stu-id="26fa0-992">Method existsMeanOrExists</span></span>

    public boolean existsMeanOrExists([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-993">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-993">Parameters</span></span>

<span data-ttu-id="26fa0-994">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-994">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-995">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-995">Return Value</span></span>

### <a name="method-fetchmode"></a><span data-ttu-id="26fa0-996">メソッド fetchMode</span><span class="sxs-lookup"><span data-stu-id="26fa0-996">Method fetchMode</span></span>

    public int fetchMode([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-997">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-997">Parameters</span></span>

<span data-ttu-id="26fa0-998">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-998">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-999">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-999">Return Value</span></span>

### <a name="method-fields"></a><span data-ttu-id="26fa0-1000">メソッド fields</span><span class="sxs-lookup"><span data-stu-id="26fa0-1000">Method fields</span></span>

    public QueryBuildFieldList fields()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1001">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1001">Return Value</span></span>

### <a name="method-file"></a><span data-ttu-id="26fa0-1002">メソッド file</span><span class="sxs-lookup"><span data-stu-id="26fa0-1002">Method file</span></span>

    public TableId file()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1003">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1003">Return Value</span></span>

### <a name="method-findrange"></a><span data-ttu-id="26fa0-1004">メソッド findRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-1004">Method findRange</span></span>

    public QueryBuildRange findRange(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1005">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1005">Parameters</span></span>

<span data-ttu-id="26fa0-1006">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1006">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1007">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1007">occurrence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1008">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1008">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1009">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1009">Return Value</span></span>

### <a name="method-firstfast"></a><span data-ttu-id="26fa0-1010">メソッド firstFast</span><span class="sxs-lookup"><span data-stu-id="26fa0-1010">Method firstFast</span></span>

<span data-ttu-id="26fa0-1011">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1011">Determines whether to retrieve the first record from the query before the other records.</span></span>

    public boolean firstFast([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1012">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1012">Parameters</span></span>

<span data-ttu-id="26fa0-1013">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1013">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1014">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1014">Return Value</span></span>

<span data-ttu-id="26fa0-1015">最初のレコードが最初に取得される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1015">true if the first record is retrieved first; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1016">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1016">Remarks</span></span>

<span data-ttu-id="26fa0-1017">firstFast プロパティは、一部のデータベース システムでレコードの取得を最適化できるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1017">The firstFast property enables some database systems to optimize record retrieval, which improves performance.</span></span> <span data-ttu-id="26fa0-1018">データベースはこのプロパティをサポートしていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1018">If the database does not support this property, it is ignored.</span></span>

### <a name="method-firstonly"></a><span data-ttu-id="26fa0-1019">メソッド firstOnly</span><span class="sxs-lookup"><span data-stu-id="26fa0-1019">Method firstOnly</span></span>

    public boolean firstOnly([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1020">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1020">Parameters</span></span>

<span data-ttu-id="26fa0-1021">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1021">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1022">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1022">Return Value</span></span>

### <a name="method-getmostrestrictedquerybuildrangestatus"></a><span data-ttu-id="26fa0-1023">メソッド getMostRestrictedQueryBuildRangeStatus</span><span class="sxs-lookup"><span data-stu-id="26fa0-1023">Method getMostRestrictedQueryBuildRangeStatus</span></span>

    public int getMostRestrictedQueryBuildRangeStatus(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1024">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1024">Parameters</span></span>

<span data-ttu-id="26fa0-1025">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1025">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1026">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1026">occurrence</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1027">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1027">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1028">Return Value</span></span>

### <a name="method-getno"></a><span data-ttu-id="26fa0-1029">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1029">Method getNo</span></span>

    public Common getNo()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1030">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1030">Return Value</span></span>

### <a name="method-id"></a><span data-ttu-id="26fa0-1031">メソッド id</span><span class="sxs-lookup"><span data-stu-id="26fa0-1031">Method id</span></span>

    public int id()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1032">Return Value</span></span>

### <a name="method-indexishint"></a><span data-ttu-id="26fa0-1033">メソッド indexIsHint</span><span class="sxs-lookup"><span data-stu-id="26fa0-1033">Method indexIsHint</span></span>

    public boolean indexIsHint(boolean arg)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1034">Parameters</span></span>

<span data-ttu-id="26fa0-1035">arg</span><span class="sxs-lookup"><span data-stu-id="26fa0-1035">arg</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1036">Return Value</span></span>

### <a name="method-ispartofsubqueryinbasequery"></a><span data-ttu-id="26fa0-1037">メソッド isPartOfSubQueryInBaseQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-1037">Method isPartOfSubQueryInBaseQuery</span></span>

    public boolean isPartOfSubQueryInBaseQuery()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1038">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1038">Return Value</span></span>

### <a name="method-joined"></a><span data-ttu-id="26fa0-1039">メソッド joined</span><span class="sxs-lookup"><span data-stu-id="26fa0-1039">Method joined</span></span>

    public boolean joined()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1040">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1040">Return Value</span></span>

### <a name="method-joineddatasources"></a><span data-ttu-id="26fa0-1041">メソッド joinedDataSources</span><span class="sxs-lookup"><span data-stu-id="26fa0-1041">Method joinedDataSources</span></span>

    public container joinedDataSources()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1042">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1042">Return Value</span></span>

### <a name="method-joinmode"></a><span data-ttu-id="26fa0-1043">メソッド joinMode</span><span class="sxs-lookup"><span data-stu-id="26fa0-1043">Method joinMode</span></span>

    public int joinMode([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1044">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1044">Parameters</span></span>

<span data-ttu-id="26fa0-1045">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1045">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1046">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1046">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="26fa0-1047">メソッド label</span><span class="sxs-lookup"><span data-stu-id="26fa0-1047">Method label</span></span>

<span data-ttu-id="26fa0-1048">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1048">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1049">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1049">Parameters</span></span>

<span data-ttu-id="26fa0-1050">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1050">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1051">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1051">Return Value</span></span>

<span data-ttu-id="26fa0-1052">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1052">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1053">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1053">Remarks</span></span>

<span data-ttu-id="26fa0-1054">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1054">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="26fa0-1055">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1055">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-level"></a><span data-ttu-id="26fa0-1056">メソッド level</span><span class="sxs-lookup"><span data-stu-id="26fa0-1056">Method level</span></span>

    public int level()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1057">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1057">Return Value</span></span>

### <a name="method-link"></a><span data-ttu-id="26fa0-1058">メソッド link</span><span class="sxs-lookup"><span data-stu-id="26fa0-1058">Method link</span></span>

    public QueryBuildLink link(int associationNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1059">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1059">Parameters</span></span>

<span data-ttu-id="26fa0-1060">associationNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1060">associationNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1061">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1061">Return Value</span></span>

### <a name="method-linkcount"></a><span data-ttu-id="26fa0-1062">メソッド linkCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1062">Method linkCount</span></span>

    public int linkCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1063">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1063">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="26fa0-1064">メソッド名</span><span class="sxs-lookup"><span data-stu-id="26fa0-1064">Method name</span></span>

<span data-ttu-id="26fa0-1065">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1065">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1066">Parameters</span></span>

<span data-ttu-id="26fa0-1067">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1067">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1068">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1068">Return Value</span></span>

<span data-ttu-id="26fa0-1069">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1069">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1070">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1070">Remarks</span></span>

<span data-ttu-id="26fa0-1071">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1071">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="26fa0-1072">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1072">Begins with a letter.</span></span>
-   <span data-ttu-id="26fa0-1073">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1073">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="26fa0-1074">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1074">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="26fa0-1075">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1075">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="26fa0-1076">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1076">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-onetoonedatasources"></a><span data-ttu-id="26fa0-1077">メソッド oneToOneDataSources</span><span class="sxs-lookup"><span data-stu-id="26fa0-1077">Method oneToOneDataSources</span></span>

    public container oneToOneDataSources()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1078">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1078">Return Value</span></span>

### <a name="method-ordermode"></a><span data-ttu-id="26fa0-1079">メソッド orderMode</span><span class="sxs-lookup"><span data-stu-id="26fa0-1079">Method orderMode</span></span>

    public int orderMode([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1080">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1080">Parameters</span></span>

<span data-ttu-id="26fa0-1081">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1081">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1082">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1082">Return Value</span></span>

### <a name="method-parentdatasource"></a><span data-ttu-id="26fa0-1083">メソッド parentDataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1083">Method parentDataSource</span></span>

    public QueryBuildDataSource parentDataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1084">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1084">Return Value</span></span>

### <a name="method-policycontext"></a><span data-ttu-id="26fa0-1085">メソッド policyContext</span><span class="sxs-lookup"><span data-stu-id="26fa0-1085">Method policyContext</span></span>

    public str policyContext([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1086">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1086">Parameters</span></span>

<span data-ttu-id="26fa0-1087">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1087">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1088">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1088">Return Value</span></span>

### <a name="method-range"></a><span data-ttu-id="26fa0-1089">メソッド range</span><span class="sxs-lookup"><span data-stu-id="26fa0-1089">Method range</span></span>

    public QueryBuildRange range(int rangeNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1090">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1090">Parameters</span></span>

<span data-ttu-id="26fa0-1091">rangeNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1091">rangeNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1092">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1092">Return Value</span></span>

### <a name="method-rangecount"></a><span data-ttu-id="26fa0-1093">メソッド rangeCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1093">Method rangeCount</span></span>

    public int rangeCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1094">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1094">Return Value</span></span>

### <a name="method-rangefield"></a><span data-ttu-id="26fa0-1095">メソッド rangeField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1095">Method rangeField</span></span>

    public QueryBuildRange rangeField(FieldId field, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1096">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1096">Parameters</span></span>

<span data-ttu-id="26fa0-1097">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1097">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1098">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1098">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1099">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1099">Return Value</span></span>

### <a name="method-relations"></a><span data-ttu-id="26fa0-1100">メソッド relations</span><span class="sxs-lookup"><span data-stu-id="26fa0-1100">Method relations</span></span>

    public boolean relations([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1101">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1101">Parameters</span></span>

<span data-ttu-id="26fa0-1102">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1102">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1103">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1103">Return Value</span></span>

### <a name="method-selectioncount"></a><span data-ttu-id="26fa0-1104">メソッド selectionCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1104">Method selectionCount</span></span>

    public int selectionCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1105">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1105">Return Value</span></span>

### <a name="method-selectwithrepeatableread"></a><span data-ttu-id="26fa0-1106">メソッド selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="26fa0-1106">Method selectWithRepeatableRead</span></span>

    public boolean selectWithRepeatableRead([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1107">Parameters</span></span>

<span data-ttu-id="26fa0-1108">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1108">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1109">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1109">Return Value</span></span>

### <a name="method-sortdirection"></a><span data-ttu-id="26fa0-1110">メソッド sortDirection</span><span class="sxs-lookup"><span data-stu-id="26fa0-1110">Method sortDirection</span></span>

    public SortOrder sortDirection(FieldId field, [SortOrder direction])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1111">Parameters</span></span>

<span data-ttu-id="26fa0-1112">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1112">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1113">direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-1113">direction</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1114">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1114">Return Value</span></span>

### <a name="method-sortfield"></a><span data-ttu-id="26fa0-1115">メソッド sortField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1115">Method sortField</span></span>

    public FieldId sortField(FieldId field)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1116">Parameters</span></span>

<span data-ttu-id="26fa0-1117">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1117">field</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1118">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1118">Return Value</span></span>

### <a name="method-sortfieldcount"></a><span data-ttu-id="26fa0-1119">メソッド sortFieldCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1119">Method sortFieldCount</span></span>

    public int sortFieldCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1120">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1120">Return Value</span></span>

### <a name="method-sortindex"></a><span data-ttu-id="26fa0-1121">メソッド sortIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1121">Method sortIndex</span></span>

    public IndexId sortIndex(int indexNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1122">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1122">Parameters</span></span>

<span data-ttu-id="26fa0-1123">indexNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1123">indexNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1124">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1124">Return Value</span></span>

### <a name="method-sortindexcount"></a><span data-ttu-id="26fa0-1125">メソッド sortIndexCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1125">Method sortIndexCount</span></span>

    public int sortIndexCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1126">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1126">Return Value</span></span>

### <a name="method-staticlink"></a><span data-ttu-id="26fa0-1127">メソッド staticlink</span><span class="sxs-lookup"><span data-stu-id="26fa0-1127">Method staticlink</span></span>

<span data-ttu-id="26fa0-1128">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1128">Returns a static Link object on the query’s data source.</span></span>

    public QueryBuildStaticlink staticlink(int staticlinkNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1129">Parameters</span></span>

<span data-ttu-id="26fa0-1130">staticlinkNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1130">staticlinkNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1131">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1131">Return Value</span></span>

<span data-ttu-id="26fa0-1132">\_staticLinkNo インデックスの静的リンク オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1132">The static Link object at the \_staticLinkNo index.</span></span>

### <a name="method-staticlinkcount"></a><span data-ttu-id="26fa0-1133">メソッド staticlinkCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1133">Method staticlinkCount</span></span>

<span data-ttu-id="26fa0-1134">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1134">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>

    public int staticlinkCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1135">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1135">Return Value</span></span>

<span data-ttu-id="26fa0-1136">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1136">The number of static links that are defined on the QueryBuildDataSource object.</span></span>

### <a name="method-table"></a><span data-ttu-id="26fa0-1137">メソッド table</span><span class="sxs-lookup"><span data-stu-id="26fa0-1137">Method table</span></span>

<span data-ttu-id="26fa0-1138">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1138">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1139">Parameters</span></span>

<span data-ttu-id="26fa0-1140">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1140">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1141">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1141">Return Value</span></span>

<span data-ttu-id="26fa0-1142">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1142">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-1143">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-1143">Method toString</span></span>

<span data-ttu-id="26fa0-1144">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1144">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1145">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1145">Return Value</span></span>

<span data-ttu-id="26fa0-1146">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1146">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1147">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1147">Remarks</span></span>

<span data-ttu-id="26fa0-1148">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1148">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-1149">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1149">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-1150">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1150">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-uniontype"></a><span data-ttu-id="26fa0-1151">メソッド unionType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1151">Method unionType</span></span>

    public int unionType([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1152">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1152">Parameters</span></span>

<span data-ttu-id="26fa0-1153">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1153">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1154">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1154">Return Value</span></span>

### <a name="method-uniqueid"></a><span data-ttu-id="26fa0-1155">メソッド uniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-1155">Method uniqueId</span></span>

    public int uniqueId()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1156">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1156">Return Value</span></span>

### <a name="method-update"></a><span data-ttu-id="26fa0-1157">メソッド update</span><span class="sxs-lookup"><span data-stu-id="26fa0-1157">Method update</span></span>

<span data-ttu-id="26fa0-1158">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1158">Determines whether the records fetched by this data source can be updated.</span></span>

    public boolean update([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1159">Parameters</span></span>

<span data-ttu-id="26fa0-1160">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1160">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1161">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1161">Return Value</span></span>

<span data-ttu-id="26fa0-1162">レコードを更新することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1162">true if the records can be updated; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1163">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1163">Remarks</span></span>

<span data-ttu-id="26fa0-1164">レコードを更新するには、ttsBegin および ttsCommit メソッドを使用して別のトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1164">To update the records, start a separate transaction by using the ttsBegin and ttsCommit methods.</span></span>

### <a name="method-clearlinks"></a><span data-ttu-id="26fa0-1165">メソッド clearLinks</span><span class="sxs-lookup"><span data-stu-id="26fa0-1165">Method clearLinks</span></span>

    public void clearLinks()

### <a name="method-cleardynalinks"></a><span data-ttu-id="26fa0-1166">メソッド clearDynalinks</span><span class="sxs-lookup"><span data-stu-id="26fa0-1166">Method clearDynalinks</span></span>

    public void clearDynalinks()

### <a name="method-clearrange"></a><span data-ttu-id="26fa0-1167">メソッド clearRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-1167">Method clearRange</span></span>

    public void clearRange(FieldId field, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1168">Parameters</span></span>

<span data-ttu-id="26fa0-1169">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1169">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1170">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1170">occurrence</span></span>  

### <a name="method-sortclear"></a><span data-ttu-id="26fa0-1171">メソッド sortClear</span><span class="sxs-lookup"><span data-stu-id="26fa0-1171">Method sortClear</span></span>

    public void sortClear()

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1172">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1172">Method finalize</span></span>

    public void finalize()

### <a name="method-addselectionfieldwithalias"></a><span data-ttu-id="26fa0-1173">メソッド addSelectionFieldWithAlias</span><span class="sxs-lookup"><span data-stu-id="26fa0-1173">Method addSelectionFieldWithAlias</span></span>

    public void addSelectionFieldWithAlias(str alias, FieldId field, [SelectionField fieldType])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1174">Parameters</span></span>

<span data-ttu-id="26fa0-1175">エイリアス</span><span class="sxs-lookup"><span data-stu-id="26fa0-1175">alias</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1176">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1176">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1177">fieldType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1177">fieldType</span></span>  

### <a name="method-addcalculationfield"></a><span data-ttu-id="26fa0-1178">メソッド addCalculationField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1178">Method addCalculationField</span></span>

    public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1179">Parameters</span></span>

<span data-ttu-id="26fa0-1180">計算</span><span class="sxs-lookup"><span data-stu-id="26fa0-1180">calculation</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1181">エイリアス</span><span class="sxs-lookup"><span data-stu-id="26fa0-1181">alias</span></span>  

### <a name="method-addforeignkeydynalink"></a><span data-ttu-id="26fa0-1182">メソッド addForeignKeyDynalink</span><span class="sxs-lookup"><span data-stu-id="26fa0-1182">Method addForeignKeyDynalink</span></span>

    public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1183">Parameters</span></span>

<span data-ttu-id="26fa0-1184">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="26fa0-1184">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1185">relatedRole</span><span class="sxs-lookup"><span data-stu-id="26fa0-1185">relatedRole</span></span>  

### <a name="method-addrelation"></a><span data-ttu-id="26fa0-1186">メソッド addRelation</span><span class="sxs-lookup"><span data-stu-id="26fa0-1186">Method addRelation</span></span>

    public void addRelation(DictRelation relation, [TableScope tableScope])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1187">Parameters</span></span>

<span data-ttu-id="26fa0-1188">関係</span><span class="sxs-lookup"><span data-stu-id="26fa0-1188">relation</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1189">tableScope</span><span class="sxs-lookup"><span data-stu-id="26fa0-1189">tableScope</span></span>  

### <a name="method-clearsortindex"></a><span data-ttu-id="26fa0-1190">メソッド clearSortIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1190">Method clearSortIndex</span></span>

    public void clearSortIndex()

### <a name="method-clearranges"></a><span data-ttu-id="26fa0-1191">メソッド clearRanges</span><span class="sxs-lookup"><span data-stu-id="26fa0-1191">Method clearRanges</span></span>

<span data-ttu-id="26fa0-1192">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1192">Deletes all ranges that are associated with the data source.</span></span>

    public void clearRanges()

#### <a name="examples"></a><span data-ttu-id="26fa0-1193">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1193">Examples</span></span>

<span data-ttu-id="26fa0-1194">次の例では、範囲を追加し、データソースから範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1194">The following example adds ranges and then removes them from a data source.</span></span>

    Query Q = new Query(); 
    QueryBuildDataSource ds = q.addDataSource(TableNum(CustTable)); 
    QueryBuildRange r = ds.addRange(FieldNum(CustTable, recId)); 
    print ds.rangeCount(); 
    ds.clearRanges(); 
    print ds.rangeCount(); 
    pause;

### <a name="method-linkfields"></a><span data-ttu-id="26fa0-1195">メソッド linkFields</span><span class="sxs-lookup"><span data-stu-id="26fa0-1195">Method linkFields</span></span>

    public void linkFields(str parentField, str thisField, [str parentDatasourceName])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1196">Parameters</span></span>

<span data-ttu-id="26fa0-1197">parentField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1197">parentField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1198">thisField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1198">thisField</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1199">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1199">parentDatasourceName</span></span>  

### <a name="method-addselectionfield"></a><span data-ttu-id="26fa0-1200">メソッド addSelectionField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1200">Method addSelectionField</span></span>

    public void addSelectionField(FieldId field, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1201">Parameters</span></span>

<span data-ttu-id="26fa0-1202">フィールド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1202">field</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1203">fieldType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1203">fieldType</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1204">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1204">arrayIndex</span></span>  

## <a name="class-querybuilddynalink"></a><span data-ttu-id="26fa0-1205">クラス QueryBuildDynalink</span><span class="sxs-lookup"><span data-stu-id="26fa0-1205">Class QueryBuildDynalink</span></span>
    class QueryBuildDynalink extends Object

### <a name="remarks"></a><span data-ttu-id="26fa0-1206">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1206">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1207">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1207">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1208">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1208">Methods</span></span>

| <span data-ttu-id="26fa0-1209">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1209">Method</span></span>                                                | <span data-ttu-id="26fa0-1210">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1210">Description</span></span> |
|-------------------------------------------------------|-------------|
| <span data-ttu-id="26fa0-1211">public Common cursor(\[Common cursor\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1211">public Common cursor(\[Common cursor\])</span></span>               |             |
| <span data-ttu-id="26fa0-1212">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1212">public QueryBuildDataSource dataSource()</span></span>              |             |
| <span data-ttu-id="26fa0-1213">public FieldId dynamicField(\[FieldId dynamicField\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1213">public FieldId dynamicField(\[FieldId dynamicField\])</span></span> |             |
| <span data-ttu-id="26fa0-1214">public FieldId field(\[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1214">public FieldId field(\[FieldId fieldId\])</span></span>             |             |
| <span data-ttu-id="26fa0-1215">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1215">public int fieldArrayIndex()</span></span>                          |             |
| <span data-ttu-id="26fa0-1216">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1216">public FieldName fieldName()</span></span>                          |             |
| <span data-ttu-id="26fa0-1217">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1217">public void finalize()</span></span>                                |             |

### <a name="method-cursor"></a><span data-ttu-id="26fa0-1218">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="26fa0-1218">Method cursor</span></span>

    public Common cursor([Common cursor])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1219">Parameters</span></span>

<span data-ttu-id="26fa0-1220">cursor</span><span class="sxs-lookup"><span data-stu-id="26fa0-1220">cursor</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1221">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1221">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1222">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1222">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1223">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1223">Return Value</span></span>

### <a name="method-dynamicfield"></a><span data-ttu-id="26fa0-1224">メソッド dynamicField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1224">Method dynamicField</span></span>

    public FieldId dynamicField([FieldId dynamicField])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1225">Parameters</span></span>

<span data-ttu-id="26fa0-1226">dynamicField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1226">dynamicField</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1227">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1227">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1228">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1228">Method field</span></span>

    public FieldId field([FieldId fieldId])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1229">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1229">Parameters</span></span>

<span data-ttu-id="26fa0-1230">fieldId</span><span class="sxs-lookup"><span data-stu-id="26fa0-1230">fieldId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1231">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1231">Return Value</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="26fa0-1232">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1232">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1233">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1233">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="26fa0-1234">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1234">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1235">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1235">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1236">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1236">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildfieldlist"></a><span data-ttu-id="26fa0-1237">クラス QueryBuildFieldList</span><span class="sxs-lookup"><span data-stu-id="26fa0-1237">Class QueryBuildFieldList</span></span>
    class QueryBuildFieldList extends TreeNode

<span data-ttu-id="26fa0-1238">QueryBuildFieldList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1238">The QueryBuildFieldList class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-1239">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1239">Remarks</span></span>

<span data-ttu-id="26fa0-1240">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1240">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1241">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1241">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1242">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1242">Methods</span></span>

| <span data-ttu-id="26fa0-1243">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1243">Method</span></span>                                                                                                 | <span data-ttu-id="26fa0-1244">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1244">Description</span></span> |
|--------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="26fa0-1245">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1245">public int addAllFields(TableName tableName)</span></span>                                                           |             |
| <span data-ttu-id="26fa0-1246">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1246">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span></span> |             |
| <span data-ttu-id="26fa0-1247">public int dynamic(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1247">public int dynamic(\[int value\])</span></span>                                                                      |             |
| <span data-ttu-id="26fa0-1248">public FieldId field(int index)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1248">public FieldId field(int index)</span></span>                                                                        |             |
| <span data-ttu-id="26fa0-1249">public int fieldCount()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1249">public int fieldCount()</span></span>                                                                                |             |
| <span data-ttu-id="26fa0-1250">public SelectionField fieldKind(int index)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1250">public SelectionField fieldKind(int index)</span></span>                                                             |             |
| <span data-ttu-id="26fa0-1251">public TableId tableSelector(int index)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1251">public TableId tableSelector(int index)</span></span>                                                                |             |
| <span data-ttu-id="26fa0-1252">public void clearFieldList()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1252">public void clearFieldList()</span></span>                                                                           |             |

### <a name="method-addallfields"></a><span data-ttu-id="26fa0-1253">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="26fa0-1253">Method addAllFields</span></span>

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1254">Parameters</span></span>

<span data-ttu-id="26fa0-1255">tableName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1255">tableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1256">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1256">Return Value</span></span>

### <a name="method-addfield"></a><span data-ttu-id="26fa0-1257">メソッド addField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1257">Method addField</span></span>

    public QueryBuildFieldList addField(FieldId fieldId, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1258">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1258">Parameters</span></span>

<span data-ttu-id="26fa0-1259">fieldId</span><span class="sxs-lookup"><span data-stu-id="26fa0-1259">fieldId</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1260">fieldType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1260">fieldType</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1261">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1261">arrayIndex</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1262">Return Value</span></span>

### <a name="method-dynamic"></a><span data-ttu-id="26fa0-1263">メソッド dynamic</span><span class="sxs-lookup"><span data-stu-id="26fa0-1263">Method dynamic</span></span>

    public int dynamic([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1264">Parameters</span></span>

<span data-ttu-id="26fa0-1265">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1265">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1266">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1266">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1267">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1267">Method field</span></span>

    public FieldId field(int index)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1268">Parameters</span></span>

<span data-ttu-id="26fa0-1269">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-1269">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1270">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1270">Return Value</span></span>

### <a name="method-fieldcount"></a><span data-ttu-id="26fa0-1271">メソッド fieldCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-1271">Method fieldCount</span></span>

    public int fieldCount()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1272">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1272">Return Value</span></span>

### <a name="method-fieldkind"></a><span data-ttu-id="26fa0-1273">メソッド fieldKind</span><span class="sxs-lookup"><span data-stu-id="26fa0-1273">Method fieldKind</span></span>

    public SelectionField fieldKind(int index)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1274">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1274">Parameters</span></span>

<span data-ttu-id="26fa0-1275">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-1275">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1276">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1276">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="26fa0-1277">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1277">Method tableSelector</span></span>

    public TableId tableSelector(int index)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1278">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1278">Parameters</span></span>

<span data-ttu-id="26fa0-1279">指数</span><span class="sxs-lookup"><span data-stu-id="26fa0-1279">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1280">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1280">Return Value</span></span>

### <a name="method-clearfieldlist"></a><span data-ttu-id="26fa0-1281">メソッド clearFieldList</span><span class="sxs-lookup"><span data-stu-id="26fa0-1281">Method clearFieldList</span></span>

    public void clearFieldList()

## <a name="class-querybuildlink"></a><span data-ttu-id="26fa0-1282">クラス QueryBuildLink</span><span class="sxs-lookup"><span data-stu-id="26fa0-1282">Class QueryBuildLink</span></span>
    class QueryBuildLink extends TreeNode

<span data-ttu-id="26fa0-1283">QueryBuildLink クラスは、X++ コードおよびメタデータの作成、読み取り、更新、および削除を可能にします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1283">The QueryBuildLink class enables for the creating, reading, updating, and deleting of X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-1284">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1284">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1285">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1285">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1286">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1286">Methods</span></span>

| <span data-ttu-id="26fa0-1287">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1287">Method</span></span>                      | <span data-ttu-id="26fa0-1288">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1288">Description</span></span> |
|-----------------------------|-------------|
| <span data-ttu-id="26fa0-1289">public int delete()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1289">public int delete()</span></span>         |             |
| <span data-ttu-id="26fa0-1290">public int field()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1290">public int field()</span></span>          |             |
| <span data-ttu-id="26fa0-1291">public boolean incomplete()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1291">public boolean incomplete()</span></span> |             |
| <span data-ttu-id="26fa0-1292">public str joinRelation()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1292">public str joinRelation()</span></span>   |             |
| <span data-ttu-id="26fa0-1293">public int relatedField()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1293">public int relatedField()</span></span>   |             |
| <span data-ttu-id="26fa0-1294">public int relatedTable()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1294">public int relatedTable()</span></span>   |             |
| <span data-ttu-id="26fa0-1295">public int table()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1295">public int table()</span></span>          |             |
| <span data-ttu-id="26fa0-1296">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1296">public void finalize()</span></span>      |             |

### <a name="method-delete"></a><span data-ttu-id="26fa0-1297">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="26fa0-1297">Method delete</span></span>

    public int delete()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1298">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1298">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1299">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1299">Method field</span></span>

    public int field()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1300">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1300">Return Value</span></span>

### <a name="method-incomplete"></a><span data-ttu-id="26fa0-1301">メソッド incomplete</span><span class="sxs-lookup"><span data-stu-id="26fa0-1301">Method incomplete</span></span>

    public boolean incomplete()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1302">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1302">Return Value</span></span>

### <a name="method-joinrelation"></a><span data-ttu-id="26fa0-1303">メソッド joinRelation</span><span class="sxs-lookup"><span data-stu-id="26fa0-1303">Method joinRelation</span></span>

    public str joinRelation()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1304">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1304">Return Value</span></span>

### <a name="method-relatedfield"></a><span data-ttu-id="26fa0-1305">メソッド relatedField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1305">Method relatedField</span></span>

    public int relatedField()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1306">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1306">Return Value</span></span>

### <a name="method-relatedtable"></a><span data-ttu-id="26fa0-1307">メソッド relatedTable</span><span class="sxs-lookup"><span data-stu-id="26fa0-1307">Method relatedTable</span></span>

    public int relatedTable()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1308">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1308">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="26fa0-1309">メソッド table</span><span class="sxs-lookup"><span data-stu-id="26fa0-1309">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1310">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1310">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1311">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1311">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildrange"></a><span data-ttu-id="26fa0-1312">クラス QueryBuildRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-1312">Class QueryBuildRange</span></span>
    class QueryBuildRange extends TreeNode

<span data-ttu-id="26fa0-1313">QueryBuildRange クラスは、QueryBuildRange クラスが関連付けられているデータ ソースからフェッチするレコードを定義する範囲を表します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1313">The QueryBuildRange class represents the ranges that define which records should be fetched from the data source in which the QueryBuildRange class is associated.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-1314">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1314">Remarks</span></span>

<span data-ttu-id="26fa0-1315">value プロパティを使用して、範囲を定義する文字列を設定できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1315">The value property can be used to set the string that defines the range.</span></span> <span data-ttu-id="26fa0-1316">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1316">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="26fa0-1317">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1317">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="26fa0-1318">特定のデータ ソースは、任意の数の範囲を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1318">A particular data source can have any number of ranges.</span></span> <span data-ttu-id="26fa0-1319">複数の範囲は、同じデータ ソース フィールドに対して有効です。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1319">Multiple ranges are valid for the same data source field.</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1320">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1320">Examples</span></span>

<span data-ttu-id="26fa0-1321">次の基本的な例は、QueryBuildRange クラスを使用して特定のデータ フィールドの対象範囲を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1321">The following basic example shows how to use the QueryBuildRange class to specify the range of interest for a specific data field.</span></span>

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

### <a name="methods"></a><span data-ttu-id="26fa0-1322">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1322">Methods</span></span>

| <span data-ttu-id="26fa0-1323">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1323">Method</span></span>                                                        | <span data-ttu-id="26fa0-1324">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1324">Description</span></span>                                                                                                                               |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fa0-1325">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1325">public QueryBuildDataSource dataSource()</span></span>                      | <span data-ttu-id="26fa0-1326">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1326">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>                                                          |
| <span data-ttu-id="26fa0-1327">public boolean doesRangeNodeBelongToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1327">public boolean doesRangeNodeBelongToCompositeQuery()</span></span>          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1328">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1328">public boolean enabled(\[boolean value\])</span></span>                     | <span data-ttu-id="26fa0-1329">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1329">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="26fa0-1330">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1330">public FieldId field(\[FieldId value\])</span></span>                       | <span data-ttu-id="26fa0-1331">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1331">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="26fa0-1332">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1332">public int fieldArrayIndex()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-1333">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1333">public FieldName fieldName()</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-1334">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1334">public str label(\[str value\])</span></span>                               | <span data-ttu-id="26fa0-1335">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1335">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="26fa0-1336">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1336">public str name(\[str value\])</span></span>                                | <span data-ttu-id="26fa0-1337">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1337">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="26fa0-1338">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1338">public str prompt()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-1339">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1339">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-1340">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1340">public int status(\[int value\])</span></span>                              | <span data-ttu-id="26fa0-1341">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1341">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="26fa0-1342">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1342">public TableId table(\[TableId value\])</span></span>                       | <span data-ttu-id="26fa0-1343">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1343">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="26fa0-1344">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1344">public TableId tableSelector(\[TableId value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="26fa0-1345">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1345">public str toString()</span></span>                                         | <span data-ttu-id="26fa0-1346">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1346">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-1347">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1347">public int typeof()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-1348">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1348">public boolean valid()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="26fa0-1349">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1349">public str value(\[str value\])</span></span>                               | <span data-ttu-id="26fa0-1350">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1350">Gets or sets the value that queried records must match to be retrieved.</span></span>                                                                   |
| <span data-ttu-id="26fa0-1351">public void associateRangeNodeToCompositeQuery()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1351">public void associateRangeNodeToCompositeQuery()</span></span>              |                                                                                                                                           |
| <span data-ttu-id="26fa0-1352">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1352">public void finalize()</span></span>                                        |                                                                                                                                           |

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1353">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1353">Method dataSource</span></span>

<span data-ttu-id="26fa0-1354">QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1354">Returns the data source that was used to instantiate the QueryBuildRange object.</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1355">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1355">Return Value</span></span>

<span data-ttu-id="26fa0-1356">QueryBuildRange クラスオブジェクトのインスタンスを作成するために使用されたデータソース。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1356">The data source that was used to instantiate the QueryBuildRange class object.</span></span>

### <a name="method-doesrangenodebelongtocompositequery"></a><span data-ttu-id="26fa0-1357">メソッド doesRangeNodeBelongToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-1357">Method doesRangeNodeBelongToCompositeQuery</span></span>

    public boolean doesRangeNodeBelongToCompositeQuery()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1358">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1358">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="26fa0-1359">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="26fa0-1359">Method enabled</span></span>

<span data-ttu-id="26fa0-1360">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1360">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1361">Parameters</span></span>

<span data-ttu-id="26fa0-1362">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1363">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1363">Return Value</span></span>

<span data-ttu-id="26fa0-1364">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1364">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1365">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1365">Remarks</span></span>

<span data-ttu-id="26fa0-1366">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1366">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="26fa0-1367">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1367">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="26fa0-1368">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1368">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1369">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1369">Method field</span></span>

<span data-ttu-id="26fa0-1370">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1370">Gets or sets the field ID associated with the object.</span></span>

    public FieldId field([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1371">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1371">Parameters</span></span>

<span data-ttu-id="26fa0-1372">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1372">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1373">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1373">Return Value</span></span>

<span data-ttu-id="26fa0-1374">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1374">The current value of the field ID associated with the object.</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="26fa0-1375">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1375">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1376">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1376">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="26fa0-1377">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1377">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1378">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1378">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="26fa0-1379">メソッド label</span><span class="sxs-lookup"><span data-stu-id="26fa0-1379">Method label</span></span>

<span data-ttu-id="26fa0-1380">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1380">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1381">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1381">Parameters</span></span>

<span data-ttu-id="26fa0-1382">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1382">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1383">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1383">Return Value</span></span>

<span data-ttu-id="26fa0-1384">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1384">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1385">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1385">Remarks</span></span>

<span data-ttu-id="26fa0-1386">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1386">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="26fa0-1387">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1387">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="26fa0-1388">メソッド名</span><span class="sxs-lookup"><span data-stu-id="26fa0-1388">Method name</span></span>

<span data-ttu-id="26fa0-1389">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1389">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1390">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1390">Parameters</span></span>

<span data-ttu-id="26fa0-1391">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1391">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1392">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1392">Return Value</span></span>

<span data-ttu-id="26fa0-1393">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1393">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1394">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1394">Remarks</span></span>

<span data-ttu-id="26fa0-1395">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1395">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="26fa0-1396">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1396">Begins with a letter.</span></span>
-   <span data-ttu-id="26fa0-1397">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1397">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="26fa0-1398">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1398">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="26fa0-1399">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1399">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="26fa0-1400">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1400">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-prompt"></a><span data-ttu-id="26fa0-1401">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="26fa0-1401">Method prompt</span></span>

    public str prompt()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1402">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1402">Return Value</span></span>

### <a name="method-rangetype"></a><span data-ttu-id="26fa0-1403">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1403">Method rangeType</span></span>

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1404">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1404">Parameters</span></span>

<span data-ttu-id="26fa0-1405">rangeType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1405">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1406">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1406">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="26fa0-1407">メソッド status</span><span class="sxs-lookup"><span data-stu-id="26fa0-1407">Method status</span></span>

<span data-ttu-id="26fa0-1408">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1408">Gets or sets the status of an object.</span></span>

    public int status([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1409">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1409">Parameters</span></span>

<span data-ttu-id="26fa0-1410">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1410">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1411">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1411">Return Value</span></span>

<span data-ttu-id="26fa0-1412">オブジェクトの現在の状態</span><span class="sxs-lookup"><span data-stu-id="26fa0-1412">The current status of the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1413">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1413">Remarks</span></span>

<span data-ttu-id="26fa0-1414">ステータスには次の値があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1414">The following values are possible for the status:</span></span>

-   <span data-ttu-id="26fa0-1415">0 - ステータス オープン。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1415">0 – Status Open.</span></span>
-   <span data-ttu-id="26fa0-1416">1 - ステータス ロック。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1416">1 – Status Lock.</span></span>
-   <span data-ttu-id="26fa0-1417">2 - ステータスが非表示です。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1417">2 – Status Hide.</span></span>

### <a name="method-table"></a><span data-ttu-id="26fa0-1418">メソッド table</span><span class="sxs-lookup"><span data-stu-id="26fa0-1418">Method table</span></span>

<span data-ttu-id="26fa0-1419">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1419">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1420">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1420">Parameters</span></span>

<span data-ttu-id="26fa0-1421">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1421">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1422">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1422">Return Value</span></span>

<span data-ttu-id="26fa0-1423">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1423">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="26fa0-1424">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1424">Method tableSelector</span></span>

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1425">Parameters</span></span>

<span data-ttu-id="26fa0-1426">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1426">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1427">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1427">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-1428">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-1428">Method toString</span></span>

<span data-ttu-id="26fa0-1429">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1429">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1430">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1430">Return Value</span></span>

<span data-ttu-id="26fa0-1431">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1431">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1432">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1432">Remarks</span></span>

<span data-ttu-id="26fa0-1433">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1433">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-1434">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1434">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-1435">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1435">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-typeof"></a><span data-ttu-id="26fa0-1436">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="26fa0-1436">Method typeof</span></span>

    public int typeof()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1437">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1437">Return Value</span></span>

### <a name="method-valid"></a><span data-ttu-id="26fa0-1438">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="26fa0-1438">Method valid</span></span>

    public boolean valid()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1439">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1439">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="26fa0-1440">メソッド value</span><span class="sxs-lookup"><span data-stu-id="26fa0-1440">Method value</span></span>

<span data-ttu-id="26fa0-1441">取得するために一致する必要がある照会されたレコードの値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1441">Gets or sets the value that queried records must match to be retrieved.</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1442">Parameters</span></span>

<span data-ttu-id="26fa0-1443">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1443">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1444">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1444">Return Value</span></span>

<span data-ttu-id="26fa0-1445">範囲の文字列値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1445">The string value for the range.</span></span>

### <a name="method-associaterangenodetocompositequery"></a><span data-ttu-id="26fa0-1446">メソッド associateRangeNodeToCompositeQuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-1446">Method associateRangeNodeToCompositeQuery</span></span>

    public void associateRangeNodeToCompositeQuery()

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1447">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1447">Method finalize</span></span>

    public void finalize()

## <a name="class-querybuildstaticlink"></a><span data-ttu-id="26fa0-1448">クラス QueryBuildStaticlink</span><span class="sxs-lookup"><span data-stu-id="26fa0-1448">Class QueryBuildStaticlink</span></span>
    class QueryBuildStaticlink extends Object

<span data-ttu-id="26fa0-1449">QueryBuildStaticLink クラスは、QueryBuildDataSource クラスで定義されている静的リンクに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1449">The QueryBuildStaticLink class provides the information about the static links that are defined on a QueryBuildDataSource class.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-1450">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1450">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1451">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1451">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1452">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1452">Methods</span></span>

| <span data-ttu-id="26fa0-1453">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1453">Method</span></span>                 | <span data-ttu-id="26fa0-1454">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1454">Description</span></span>                                                         |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="26fa0-1455">public FieldId field()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1455">public FieldId field()</span></span> | <span data-ttu-id="26fa0-1456">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="26fa0-1456">Provides the field information on which the static link is defined/</span></span> |
| <span data-ttu-id="26fa0-1457">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1457">public AnyType value()</span></span> | <span data-ttu-id="26fa0-1458">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1458">Gets the value of the field on which the static link is defined.</span></span>    |
| <span data-ttu-id="26fa0-1459">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1459">public void finalize()</span></span> |                                                                     |

### <a name="method-field"></a><span data-ttu-id="26fa0-1460">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1460">Method field</span></span>

<span data-ttu-id="26fa0-1461">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="26fa0-1461">Provides the field information on which the static link is defined/</span></span>

    public FieldId field()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1462">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1462">Return Value</span></span>

<span data-ttu-id="26fa0-1463">静的リンクが定義されているフィールドの FieldId 値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1463">The FieldId value of the field on which the static link is defined.</span></span>

### <a name="method-value"></a><span data-ttu-id="26fa0-1464">メソッド value</span><span class="sxs-lookup"><span data-stu-id="26fa0-1464">Method value</span></span>

<span data-ttu-id="26fa0-1465">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1465">Gets the value of the field on which the static link is defined.</span></span>

    public AnyType value()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1466">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1466">Return Value</span></span>

<span data-ttu-id="26fa0-1467">静的リンクの値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1467">The value of the static link.</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1468">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1468">Method finalize</span></span>

    public void finalize()

## <a name="class-queryfilter"></a><span data-ttu-id="26fa0-1469">クラス QueryFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-1469">Class QueryFilter</span></span>
    class QueryFilter extends Object

### <a name="remarks"></a><span data-ttu-id="26fa0-1470">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1470">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1471">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1471">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1472">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1472">Methods</span></span>

| <span data-ttu-id="26fa0-1473">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1473">Method</span></span>                                                        | <span data-ttu-id="26fa0-1474">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1474">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26fa0-1475">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1475">public QueryBuildDataSource dataSource()</span></span>                      |                                                      |
| <span data-ttu-id="26fa0-1476">public FieldName field()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1476">public FieldName field()</span></span>                                      |                                                      |
| <span data-ttu-id="26fa0-1477">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1477">public QueryRangeType rangeType(\[QueryRangeType rangeType\])</span></span> |                                                      |
| <span data-ttu-id="26fa0-1478">public int status(\[int status\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1478">public int status(\[int status\])</span></span>                             |                                                      |
| <span data-ttu-id="26fa0-1479">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1479">public str toString()</span></span>                                         | <span data-ttu-id="26fa0-1480">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1480">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="26fa0-1481">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1481">public str value(\[str value\])</span></span>                               |                                                      |
| <span data-ttu-id="26fa0-1482">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1482">public void finalize()</span></span>                                        |                                                      |

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1483">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1483">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1484">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1484">Return Value</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1485">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1485">Method field</span></span>

    public FieldName field()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1486">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1486">Return Value</span></span>

### <a name="method-rangetype"></a><span data-ttu-id="26fa0-1487">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1487">Method rangeType</span></span>

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1488">Parameters</span></span>

<span data-ttu-id="26fa0-1489">rangeType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1489">rangeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1490">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1490">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="26fa0-1491">メソッド status</span><span class="sxs-lookup"><span data-stu-id="26fa0-1491">Method status</span></span>

    public int status([int status])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1492">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1492">Parameters</span></span>

<span data-ttu-id="26fa0-1493">ステータス</span><span class="sxs-lookup"><span data-stu-id="26fa0-1493">status</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1494">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1494">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-1495">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-1495">Method toString</span></span>

<span data-ttu-id="26fa0-1496">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1496">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1497">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1497">Return Value</span></span>

<span data-ttu-id="26fa0-1498">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1498">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1499">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1499">Remarks</span></span>

<span data-ttu-id="26fa0-1500">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1500">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-1501">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1501">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-1502">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1502">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="26fa0-1503">メソッド value</span><span class="sxs-lookup"><span data-stu-id="26fa0-1503">Method value</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1504">Parameters</span></span>

<span data-ttu-id="26fa0-1505">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1505">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1506">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1506">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1507">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1507">Method finalize</span></span>

    public void finalize()

## <a name="class-querygroupbyfield"></a><span data-ttu-id="26fa0-1508">クラス QueryGroupByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1508">Class QueryGroupByField</span></span>
    class QueryGroupByField extends TreeNode

### <a name="remarks"></a><span data-ttu-id="26fa0-1509">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1509">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1510">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1510">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1511">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1511">Methods</span></span>

| <span data-ttu-id="26fa0-1512">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1512">Method</span></span>                                                  | <span data-ttu-id="26fa0-1513">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1513">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="26fa0-1514">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1514">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="26fa0-1515">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1515">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="26fa0-1516">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1516">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="26fa0-1517">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1517">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="26fa0-1518">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1518">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="26fa0-1519">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1519">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="26fa0-1520">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1520">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="26fa0-1521">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1521">public void finalize()</span></span>                                  |             |

### <a name="method-autoheader"></a><span data-ttu-id="26fa0-1522">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="26fa0-1522">Method autoHeader</span></span>

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1523">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1523">Parameters</span></span>

<span data-ttu-id="26fa0-1524">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1524">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1525">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1525">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="26fa0-1526">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-1526">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1527">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1527">Parameters</span></span>

<span data-ttu-id="26fa0-1528">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1528">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1529">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1529">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="26fa0-1530">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="26fa0-1530">Method autoSum</span></span>

    public boolean autoSum([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1531">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1531">Parameters</span></span>

<span data-ttu-id="26fa0-1532">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1532">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1533">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1533">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="26fa0-1534">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-1534">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1535">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1535">Parameters</span></span>

<span data-ttu-id="26fa0-1536">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1536">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1537">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1537">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1538">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1538">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1539">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1539">Return Value</span></span>

### <a name="method-fieldid"></a><span data-ttu-id="26fa0-1540">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="26fa0-1540">Method fieldID</span></span>

    public int fieldID()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1541">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1541">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="26fa0-1542">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1542">Method tableSelector</span></span>

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1543">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1543">Parameters</span></span>

<span data-ttu-id="26fa0-1544">tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1544">tableSelector</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1545">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1545">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1546">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1546">Method finalize</span></span>

    public void finalize()

## <a name="class-queryhavingfilter"></a><span data-ttu-id="26fa0-1547">クラス QueryHavingFilter</span><span class="sxs-lookup"><span data-stu-id="26fa0-1547">Class QueryHavingFilter</span></span>
    class QueryHavingFilter extends TreeNode

### <a name="remarks"></a><span data-ttu-id="26fa0-1548">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1548">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1549">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1549">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1550">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1550">Methods</span></span>

| <span data-ttu-id="26fa0-1551">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1551">Method</span></span>                                          | <span data-ttu-id="26fa0-1552">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1552">Description</span></span>                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fa0-1553">public AggregateFunction aggregateFunction()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1553">public AggregateFunction aggregateFunction()</span></span>    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1554">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1554">public QueryBuildDataSource dataSource()</span></span>        |                                                                                                                                           |
| <span data-ttu-id="26fa0-1555">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1555">public boolean enabled(\[boolean value\])</span></span>       | <span data-ttu-id="26fa0-1556">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1556">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="26fa0-1557">public FieldId field(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1557">public FieldId field(\[FieldId value\])</span></span>         | <span data-ttu-id="26fa0-1558">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1558">Gets or sets the field ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="26fa0-1559">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1559">public int fieldArrayIndex()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1560">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1560">public FieldName fieldName()</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1561">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1561">public str label(\[str value\])</span></span>                 | <span data-ttu-id="26fa0-1562">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1562">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="26fa0-1563">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1563">public str name(\[str value\])</span></span>                  | <span data-ttu-id="26fa0-1564">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1564">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="26fa0-1565">public str prompt()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1565">public str prompt()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-1566">public int status(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1566">public int status(\[int value\])</span></span>                | <span data-ttu-id="26fa0-1567">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1567">Gets or sets the status of an object.</span></span>                                                                                                     |
| <span data-ttu-id="26fa0-1568">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1568">public TableId table(\[TableId value\])</span></span>         | <span data-ttu-id="26fa0-1569">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1569">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="26fa0-1570">public TableId tableSelector(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1570">public TableId tableSelector(\[TableId value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-1571">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1571">public str toString()</span></span>                           | <span data-ttu-id="26fa0-1572">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1572">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-1573">public int typeof()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1573">public int typeof()</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-1574">public boolean valid()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1574">public boolean valid()</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1575">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1575">public str value(\[str value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-1576">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1576">public void finalize()</span></span>                          |                                                                                                                                           |

### <a name="method-aggregatefunction"></a><span data-ttu-id="26fa0-1577">メソッド aggregateFunction</span><span class="sxs-lookup"><span data-stu-id="26fa0-1577">Method aggregateFunction</span></span>

    public AggregateFunction aggregateFunction()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1578">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1578">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1579">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1579">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1580">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1580">Return Value</span></span>

### <a name="method-enabled"></a><span data-ttu-id="26fa0-1581">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="26fa0-1581">Method enabled</span></span>

<span data-ttu-id="26fa0-1582">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1582">Determines whether to enable or disable the object.</span></span>

    public boolean enabled([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1583">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1583">Parameters</span></span>

<span data-ttu-id="26fa0-1584">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1584">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1585">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1585">Return Value</span></span>

<span data-ttu-id="26fa0-1586">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1586">true if the object is enabled; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1587">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1587">Remarks</span></span>

<span data-ttu-id="26fa0-1588">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1588">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="26fa0-1589">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1589">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="26fa0-1590">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1590">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="method-field"></a><span data-ttu-id="26fa0-1591">メソッド field</span><span class="sxs-lookup"><span data-stu-id="26fa0-1591">Method field</span></span>

<span data-ttu-id="26fa0-1592">オブジェクトに関連付けられているフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1592">Gets or sets the field ID associated with the object.</span></span>

    public FieldId field([FieldId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1593">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1593">Parameters</span></span>

<span data-ttu-id="26fa0-1594">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1594">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1595">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1595">Return Value</span></span>

<span data-ttu-id="26fa0-1596">オブジェクトに関連付けられたフィールド ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1596">The current value of the field ID associated with the object.</span></span>

### <a name="method-fieldarrayindex"></a><span data-ttu-id="26fa0-1597">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="26fa0-1597">Method fieldArrayIndex</span></span>

    public int fieldArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1598">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1598">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="26fa0-1599">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1599">Method fieldName</span></span>

    public FieldName fieldName()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1600">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1600">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="26fa0-1601">メソッド label</span><span class="sxs-lookup"><span data-stu-id="26fa0-1601">Method label</span></span>

<span data-ttu-id="26fa0-1602">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1602">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1603">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1603">Parameters</span></span>

<span data-ttu-id="26fa0-1604">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1604">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1605">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1605">Return Value</span></span>

<span data-ttu-id="26fa0-1606">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1606">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1607">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1607">Remarks</span></span>

<span data-ttu-id="26fa0-1608">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1608">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="26fa0-1609">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1609">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-name"></a><span data-ttu-id="26fa0-1610">メソッド名</span><span class="sxs-lookup"><span data-stu-id="26fa0-1610">Method name</span></span>

<span data-ttu-id="26fa0-1611">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1611">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1612">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1612">Parameters</span></span>

<span data-ttu-id="26fa0-1613">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1613">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1614">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1614">Return Value</span></span>

<span data-ttu-id="26fa0-1615">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1615">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1616">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1616">Remarks</span></span>

<span data-ttu-id="26fa0-1617">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1617">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="26fa0-1618">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1618">Begins with a letter.</span></span>
-   <span data-ttu-id="26fa0-1619">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1619">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="26fa0-1620">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1620">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="26fa0-1621">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1621">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="26fa0-1622">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1622">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

### <a name="method-prompt"></a><span data-ttu-id="26fa0-1623">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="26fa0-1623">Method prompt</span></span>

    public str prompt()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1624">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1624">Return Value</span></span>

### <a name="method-status"></a><span data-ttu-id="26fa0-1625">メソッド status</span><span class="sxs-lookup"><span data-stu-id="26fa0-1625">Method status</span></span>

<span data-ttu-id="26fa0-1626">オブジェクトの状態を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1626">Gets or sets the status of an object.</span></span>

    public int status([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1627">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1627">Parameters</span></span>

<span data-ttu-id="26fa0-1628">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1628">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1629">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1629">Return Value</span></span>

<span data-ttu-id="26fa0-1630">オブジェクトのステータスの現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1630">The current value of the status of the object.</span></span>

### <a name="method-table"></a><span data-ttu-id="26fa0-1631">メソッド table</span><span class="sxs-lookup"><span data-stu-id="26fa0-1631">Method table</span></span>

<span data-ttu-id="26fa0-1632">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1632">Gets or sets the table ID that is associated with the object.</span></span>

    public TableId table([TableId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1633">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1633">Parameters</span></span>

<span data-ttu-id="26fa0-1634">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1634">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1635">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1635">Return Value</span></span>

<span data-ttu-id="26fa0-1636">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1636">The current value of the table ID that is associated with the object.</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="26fa0-1637">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1637">Method tableSelector</span></span>

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1638">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1638">Parameters</span></span>

<span data-ttu-id="26fa0-1639">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1639">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1640">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1640">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-1641">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-1641">Method toString</span></span>

<span data-ttu-id="26fa0-1642">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1642">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1643">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1643">Return Value</span></span>

<span data-ttu-id="26fa0-1644">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1644">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1645">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1645">Remarks</span></span>

<span data-ttu-id="26fa0-1646">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1646">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-1647">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1647">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-1648">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1648">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-typeof"></a><span data-ttu-id="26fa0-1649">メソッド typeof</span><span class="sxs-lookup"><span data-stu-id="26fa0-1649">Method typeof</span></span>

    public int typeof()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1650">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1650">Return Value</span></span>

### <a name="method-valid"></a><span data-ttu-id="26fa0-1651">メソッド valid</span><span class="sxs-lookup"><span data-stu-id="26fa0-1651">Method valid</span></span>

    public boolean valid()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1652">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1652">Return Value</span></span>

### <a name="method-value"></a><span data-ttu-id="26fa0-1653">メソッド value</span><span class="sxs-lookup"><span data-stu-id="26fa0-1653">Method value</span></span>

    public str value([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1654">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1654">Parameters</span></span>

<span data-ttu-id="26fa0-1655">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1655">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1656">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1656">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1657">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1657">Method finalize</span></span>

    public void finalize()

## <a name="class-queryorderbyfield"></a><span data-ttu-id="26fa0-1658">クラス QueryOrderByField</span><span class="sxs-lookup"><span data-stu-id="26fa0-1658">Class QueryOrderByField</span></span>
    class QueryOrderByField extends TreeNode

### <a name="remarks"></a><span data-ttu-id="26fa0-1659">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1659">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1660">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1660">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="26fa0-1661">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1661">Methods</span></span>

| <span data-ttu-id="26fa0-1662">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1662">Method</span></span>                                                  | <span data-ttu-id="26fa0-1663">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1663">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="26fa0-1664">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1664">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="26fa0-1665">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1665">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="26fa0-1666">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1666">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="26fa0-1667">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1667">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="26fa0-1668">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1668">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="26fa0-1669">public SortOrder direction()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1669">public SortOrder direction()</span></span>                            |             |
| <span data-ttu-id="26fa0-1670">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1670">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="26fa0-1671">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1671">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="26fa0-1672">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1672">public void finalize()</span></span>                                  |             |

### <a name="method-autoheader"></a><span data-ttu-id="26fa0-1673">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="26fa0-1673">Method autoHeader</span></span>

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1674">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1674">Parameters</span></span>

<span data-ttu-id="26fa0-1675">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1675">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1676">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1676">Return Value</span></span>

### <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="26fa0-1677">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-1677">Method autoHeaderDetailLevel</span></span>

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1678">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1678">Parameters</span></span>

<span data-ttu-id="26fa0-1679">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1679">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1680">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1680">Return Value</span></span>

### <a name="method-autosum"></a><span data-ttu-id="26fa0-1681">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="26fa0-1681">Method autoSum</span></span>

    public boolean autoSum([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1682">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1682">Parameters</span></span>

<span data-ttu-id="26fa0-1683">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1683">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1684">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1684">Return Value</span></span>

### <a name="method-autosumdetaillevel"></a><span data-ttu-id="26fa0-1685">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="26fa0-1685">Method autoSumDetailLevel</span></span>

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1686">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1686">Parameters</span></span>

<span data-ttu-id="26fa0-1687">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1687">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1688">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1688">Return Value</span></span>

### <a name="method-datasource"></a><span data-ttu-id="26fa0-1689">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="26fa0-1689">Method dataSource</span></span>

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1690">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1690">Return Value</span></span>

### <a name="method-direction"></a><span data-ttu-id="26fa0-1691">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="26fa0-1691">Method direction</span></span>

    public SortOrder direction()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1692">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1692">Return Value</span></span>

### <a name="method-fieldid"></a><span data-ttu-id="26fa0-1693">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="26fa0-1693">Method fieldID</span></span>

    public int fieldID()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1694">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1694">Return Value</span></span>

### <a name="method-tableselector"></a><span data-ttu-id="26fa0-1695">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1695">Method tableSelector</span></span>

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1696">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1696">Parameters</span></span>

<span data-ttu-id="26fa0-1697">tableSelector</span><span class="sxs-lookup"><span data-stu-id="26fa0-1697">tableSelector</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1698">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1698">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="26fa0-1699">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="26fa0-1699">Method finalize</span></span>

    public void finalize()

## <a name="class-queryrun"></a><span data-ttu-id="26fa0-1700">クラス QueryRun</span><span class="sxs-lookup"><span data-stu-id="26fa0-1700">Class QueryRun</span></span>
    class QueryRun extends ObjectRun

<span data-ttu-id="26fa0-1701">QueryRun クラスは、データベース内のテーブルをスキャンし、ユーザーによって与えられている制約を満たすレコードをフェッチして、ユーザー入力からこのような制約を収集するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1701">The QueryRun class traverses tables in the database, fetches records that satisfy constraints that are given by the user, and helps to gather such constraints from user input.</span></span>

### <a name="remarks"></a><span data-ttu-id="26fa0-1702">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1702">Remarks</span></span>

<span data-ttu-id="26fa0-1703">QueryRun オブジェクトは、データベース内のテーブルをスキャンし、ユーザーが指定した制約を満たすレコードをフェッチするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1703">QueryRun objects are used to traverse tables in the database and fetch records that satisfy the constraints that are given by the user.</span></span> <span data-ttu-id="26fa0-1704">QueryRun オブジェクトは、ユーザーがそのような制限を入力できるように、ユーザーと通信することができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1704">A QueryRun object may interact with the user to let the user enter such constraints.</span></span> <span data-ttu-id="26fa0-1705">クエリは、レポートに表示するデータを記述してフェッチするためにレポートにより内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1705">Queries are used internally by reports to delineate and fetch the data to be presented in the report.</span></span> <span data-ttu-id="26fa0-1706">QueryRun オブジェクトは、クエリ オブジェクト を使用してクエリの構造を定義します (たとえば、どのテーブルを検索するか、レコードをどのように並び替えるかなど)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1706">A QueryRun object relies on a Query object to define the structure of the query (for example, which tables are searched and how the records are sorted).</span></span> <span data-ttu-id="26fa0-1707">QueryRun オブジェクトは、クエリの動的動作を定義しますが、クエリ オブジェクトはクエリの静的特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1707">A QueryRun object defines the dynamic behavior of the query, whereas a Query object defines the static characteristics of the query.</span></span>

### <a name="examples"></a><span data-ttu-id="26fa0-1708">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1708">Examples</span></span>

<span data-ttu-id="26fa0-1709">次の例では、Finance and Operations のアプリケーション オブジェクト ツリー (AOT) での顧客という名前のクエリがあり、そこに 1 つのデータ ソース CustTable テーブルがあると見なされます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1709">In the following example, it is assumed that there is a query named Customer in the Finance and Operations Application Object Tree (AOT), and that it has one data source, the CustTable table.</span></span>

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

### <a name="methods"></a><span data-ttu-id="26fa0-1710">メソッド</span><span class="sxs-lookup"><span data-stu-id="26fa0-1710">Methods</span></span>

| <span data-ttu-id="26fa0-1711">方法</span><span class="sxs-lookup"><span data-stu-id="26fa0-1711">Method</span></span>                                                                                                         | <span data-ttu-id="26fa0-1712">説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1712">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fa0-1713">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1713">public boolean allowCheck(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-1714">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1714">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-1715">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1715">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-1716">public boolean changed(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1716">public boolean changed(TableId table, \[int occurrence\])</span></span>                                                      | <span data-ttu-id="26fa0-1717">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1717">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>                     |
| <span data-ttu-id="26fa0-1718">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1718">public str changedBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="26fa0-1719">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1719">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="26fa0-1720">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1720">public Date changedDate(\[Date value\])</span></span>                                                                        | <span data-ttu-id="26fa0-1721">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1721">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="26fa0-1722">public boolean changedNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1722">public boolean changedNo(int dataSourceNo)</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-1723">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1723">public str changedTime(\[str value\])</span></span>                                                                          | <span data-ttu-id="26fa0-1724">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1724">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="26fa0-1725">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1725">public str createdBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="26fa0-1726">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1726">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="26fa0-1727">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1727">public Date creationDate(\[Date value\])</span></span>                                                                       | <span data-ttu-id="26fa0-1728">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1728">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="26fa0-1729">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1729">public str creationTime(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-1730">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1730">public str description(\[str value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1731">public boolean equal(Object obj)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1731">public boolean equal(Object obj)</span></span>                                                                               | <span data-ttu-id="26fa0-1732">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1732">Determines whether the specified object is equal to the current object.</span></span>                                                                   |
| <span data-ttu-id="26fa0-1733">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1733">public str form(\[str value\])</span></span>                                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-1734">public Common get(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1734">public Common get(TableId table, \[int occurrence\])</span></span>                                                           | <span data-ttu-id="26fa0-1735">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1735">Retrieves the record fetched by the previous call to next method.</span></span>                                                                         |
| <span data-ttu-id="26fa0-1736">public System.Type getImpExpDataContractType()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1736">public System.Type getImpExpDataContractType()</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-1737">public Common getNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1737">public Common getNo(int dataSourceNo)</span></span>                                                                          | <span data-ttu-id="26fa0-1738">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1738">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>                                                                |
| <span data-ttu-id="26fa0-1739">public boolean importable()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1739">public boolean importable()</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1740">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1740">public boolean interactive(\[boolean value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="26fa0-1741">public boolean isPositionPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1741">public boolean isPositionPagingEnabled()</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="26fa0-1742">public boolean isQueryTimedout()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1742">public boolean isQueryTimedout()</span></span>                                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-1743">public boolean isValueBasedPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1743">public boolean isValueBasedPagingEnabled()</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-1744">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1744">public int literals(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-1745">public Guid loadCsv(str fileName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1745">public Guid loadCsv(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-1746">public Guid loadXml(str fileName)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1746">public Guid loadXml(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-1747">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1747">public str name(\[str value\])</span></span>                                                                                 | <span data-ttu-id="26fa0-1748">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1748">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="26fa0-1749">public QueryRun newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1749">public QueryRun newObject(AnyType source)</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-1750">public boolean next()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1750">public boolean next()</span></span>                                                                                          | <span data-ttu-id="26fa0-1751">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1751">Retrieves the next record from the query.</span></span>                                                                                                 |
| <span data-ttu-id="26fa0-1752">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1752">public int nextUniqueId(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-1753">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1753">public Guid origin(\[Guid value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-1754">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1754">public container pack(\[boolean doCheck\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="26fa0-1755">public boolean prompt()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1755">public boolean prompt()</span></span>                                                                                        | <span data-ttu-id="26fa0-1756">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1756">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>                                                   |
| <span data-ttu-id="26fa0-1757">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1757">public Query query(\[Query query\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-1758">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1758">public int queryType(\[int value\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-1759">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1759">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1760">public ReportRun report()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1760">public ReportRun report()</span></span>                                                                                      |                                                                                                                                           |
| <span data-ttu-id="26fa0-1761">public ReportRun reportRun()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1761">public ReportRun reportRun()</span></span>                                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-1762">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1762">public boolean saved()</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-1763">public boolean saveUserSetup(\[boolean saveIt\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1763">public boolean saveUserSetup(\[boolean saveIt\])</span></span>                                                               | <span data-ttu-id="26fa0-1764">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1764">Saves the user setup.</span></span>                                                                                                                     |
| <span data-ttu-id="26fa0-1765">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1765">public boolean searchable(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-1766">public boolean setCursor(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1766">public boolean setCursor(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1767">public boolean setRecord(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1767">public boolean setRecord(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="26fa0-1768">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1768">public str title(\[str value\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="26fa0-1769">public str toString()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1769">public str toString()</span></span>                                                                                          | <span data-ttu-id="26fa0-1770">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1770">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="26fa0-1771">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1771">public boolean userUpdate(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="26fa0-1772">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1772">public int version(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="26fa0-1773">::public static int getQueryRowCount(Query query, int maxRows)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1773">::public static int getQueryRowCount(Query query, int maxRows)</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-1774">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1774">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span></span> |                                                                                                                                           |
| <span data-ttu-id="26fa0-1775">public void run()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1775">public void run()</span></span>                                                                                              | <span data-ttu-id="26fa0-1776">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1776">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>                                  |
| <span data-ttu-id="26fa0-1777">public void new(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1777">public void new(AnyType source)</span></span>                                                                                | <span data-ttu-id="26fa0-1778">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1778">Initializes a new instance of the Object class.</span></span>                                                                                           |
| <span data-ttu-id="26fa0-1779">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1779">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-1780">public void reset()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1780">public void reset()</span></span>                                                                                            |                                                                                                                                           |
| <span data-ttu-id="26fa0-1781">public void setImportSession(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1781">public void setImportSession(Guid importSession)</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="26fa0-1782">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1782">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="26fa0-1783">public void init()</span><span class="sxs-lookup"><span data-stu-id="26fa0-1783">public void init()</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="26fa0-1784">public void enablePositionPaging(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1784">public void enablePositionPaging(\[boolean enabled\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1785">public void shred(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="26fa0-1785">public void shred(Guid importSession)</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="26fa0-1786">public void enableValueBasedPaging(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1786">public void enableValueBasedPaging(\[boolean enable\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="26fa0-1787">public void bulkNext(\[boolean fetchAllData\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1787">public void bulkNext(\[boolean fetchAllData\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="26fa0-1788">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span><span class="sxs-lookup"><span data-stu-id="26fa0-1788">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span></span>                              |                                                                                                                                           |

### <a name="method-allowcheck"></a><span data-ttu-id="26fa0-1789">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="26fa0-1789">Method allowCheck</span></span>

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1790">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1790">Parameters</span></span>

<span data-ttu-id="26fa0-1791">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1791">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1792">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1792">Return Value</span></span>

### <a name="method-allowcrosscompany"></a><span data-ttu-id="26fa0-1793">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="26fa0-1793">Method allowCrossCompany</span></span>

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1794">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1794">Parameters</span></span>

<span data-ttu-id="26fa0-1795">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1795">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1796">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1796">Return Value</span></span>

### <a name="method-canpage"></a><span data-ttu-id="26fa0-1797">メソッド canPage</span><span class="sxs-lookup"><span data-stu-id="26fa0-1797">Method canPage</span></span>

    public boolean canPage([boolean skipOrderByCheck], [boolean throwIfNotPagable], [boolean isValuePaging])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1798">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1798">Parameters</span></span>

<span data-ttu-id="26fa0-1799">skipOrderByCheck</span><span class="sxs-lookup"><span data-stu-id="26fa0-1799">skipOrderByCheck</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1800">throwIfNotPagable</span><span class="sxs-lookup"><span data-stu-id="26fa0-1800">throwIfNotPagable</span></span>  

<!-- -->

<span data-ttu-id="26fa0-1801">isValuePaging</span><span class="sxs-lookup"><span data-stu-id="26fa0-1801">isValuePaging</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1802">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1802">Return Value</span></span>

### <a name="method-changed"></a><span data-ttu-id="26fa0-1803">メソッド changed</span><span class="sxs-lookup"><span data-stu-id="26fa0-1803">Method changed</span></span>

<span data-ttu-id="26fa0-1804">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1804">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>

    public boolean changed(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1805">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1805">Parameters</span></span>

<span data-ttu-id="26fa0-1806">テーブル</span><span class="sxs-lookup"><span data-stu-id="26fa0-1806">table</span></span>  
<span data-ttu-id="26fa0-1807">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1807">The data source to check; optional.</span></span> <span data-ttu-id="26fa0-1808">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1808">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

<!-- -->

<span data-ttu-id="26fa0-1809">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1809">occurrence</span></span>  
<span data-ttu-id="26fa0-1810">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1810">The data source to check; optional.</span></span> <span data-ttu-id="26fa0-1811">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1811">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-1812">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1812">Return Value</span></span>

<span data-ttu-id="26fa0-1813">QueryRun.next に対する最後の呼び出し後に指定データ ソースが変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1813">true if the specified data source has changed since the last call to QueryRun.next; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1814">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1814">Remarks</span></span>

<span data-ttu-id="26fa0-1815">このメソッドは、データ ソースが階層構造になっている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1815">This method is useful when data sources are hierarchically structured.</span></span> <span data-ttu-id="26fa0-1816">埋め込みデータ ソースは、何回でも変更できます (顧客トランザクションなど)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1816">A more embedded data source may change many times (such as the customer transactions).</span></span> <span data-ttu-id="26fa0-1817">これは、埋め込まれていないデータソース (顧客テーブルなど) が新しいレコード (別の顧客) をフェッチするたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1817">This occurs every time that a less embedded data source (such as the customer table) fetches a new record (another customer).</span></span> <span data-ttu-id="26fa0-1818">この関数の代わりに changedNo メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1818">The changedNo method can be used instead of this function.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="26fa0-1819">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-1819">Method changedBy</span></span>

<span data-ttu-id="26fa0-1820">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1820">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1821">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1821">Parameters</span></span>

<span data-ttu-id="26fa0-1822">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1822">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1823">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1823">Return Value</span></span>

<span data-ttu-id="26fa0-1824">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1824">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="26fa0-1825">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-1825">Method changedDate</span></span>

<span data-ttu-id="26fa0-1826">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1826">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1827">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1827">Parameters</span></span>

<span data-ttu-id="26fa0-1828">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1828">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1829">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1829">Return Value</span></span>

<span data-ttu-id="26fa0-1830">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1830">The date an application object was last changed.</span></span>

### <a name="method-changedno"></a><span data-ttu-id="26fa0-1831">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1831">Method changedNo</span></span>

    public boolean changedNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1832">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1832">Parameters</span></span>

<span data-ttu-id="26fa0-1833">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1833">dataSourceNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1834">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1834">Return Value</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="26fa0-1835">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-1835">Method changedTime</span></span>

<span data-ttu-id="26fa0-1836">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1836">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1837">Parameters</span></span>

<span data-ttu-id="26fa0-1838">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1838">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1839">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1839">Return Value</span></span>

<span data-ttu-id="26fa0-1840">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1840">The time an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="26fa0-1841">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="26fa0-1841">Method createdBy</span></span>

<span data-ttu-id="26fa0-1842">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1842">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1843">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1843">Parameters</span></span>

<span data-ttu-id="26fa0-1844">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1844">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1845">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1845">Return Value</span></span>

<span data-ttu-id="26fa0-1846">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1846">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="26fa0-1847">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="26fa0-1847">Method creationDate</span></span>

<span data-ttu-id="26fa0-1848">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1848">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1849">Parameters</span></span>

<span data-ttu-id="26fa0-1850">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1850">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1851">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1851">Return Value</span></span>

<span data-ttu-id="26fa0-1852">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1852">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="26fa0-1853">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="26fa0-1853">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1854">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1854">Parameters</span></span>

<span data-ttu-id="26fa0-1855">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1855">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1856">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1856">Return Value</span></span>

### <a name="method-description"></a><span data-ttu-id="26fa0-1857">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="26fa0-1857">Method description</span></span>

    public str description([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1858">Parameters</span></span>

<span data-ttu-id="26fa0-1859">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1859">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1860">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1860">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="26fa0-1861">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="26fa0-1861">Method equal</span></span>

<span data-ttu-id="26fa0-1862">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1862">Determines whether the specified object is equal to the current object.</span></span>

    public boolean equal(Object obj)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1863">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1863">Parameters</span></span>

<span data-ttu-id="26fa0-1864">obj</span><span class="sxs-lookup"><span data-stu-id="26fa0-1864">obj</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1865">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1865">Return Value</span></span>

<span data-ttu-id="26fa0-1866">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1866">true if the specified object is equal to the current object; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1867">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1867">Remarks</span></span>

<span data-ttu-id="26fa0-1868">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1868">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="26fa0-1869">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1869">However, derived classes can override the Object::equal method to support value equality.</span></span>

### <a name="method-form"></a><span data-ttu-id="26fa0-1870">メソッド form</span><span class="sxs-lookup"><span data-stu-id="26fa0-1870">Method form</span></span>

    public str form([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1871">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1871">Parameters</span></span>

<span data-ttu-id="26fa0-1872">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1872">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1873">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1873">Return Value</span></span>

### <a name="method-get"></a><span data-ttu-id="26fa0-1874">メソッド get</span><span class="sxs-lookup"><span data-stu-id="26fa0-1874">Method get</span></span>

<span data-ttu-id="26fa0-1875">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1875">Retrieves the record fetched by the previous call to next method.</span></span>

    public Common get(TableId table, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1876">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1876">Parameters</span></span>

<span data-ttu-id="26fa0-1877">テーブル</span><span class="sxs-lookup"><span data-stu-id="26fa0-1877">table</span></span>  
<span data-ttu-id="26fa0-1878">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1878">The data source to be addressed; optional.</span></span> <span data-ttu-id="26fa0-1879">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1879">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="26fa0-1880">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1880">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="26fa0-1881">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1881">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="26fa0-1882">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1882">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

<!-- -->

<span data-ttu-id="26fa0-1883">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-1883">occurrence</span></span>  
<span data-ttu-id="26fa0-1884">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1884">The data source to be addressed; optional.</span></span> <span data-ttu-id="26fa0-1885">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1885">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="26fa0-1886">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1886">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="26fa0-1887">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1887">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="26fa0-1888">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1888">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-1889">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1889">Return Value</span></span>

<span data-ttu-id="26fa0-1890">引数で識別されるデータ ソースからフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1890">Returns the record fetched from the data source identified by the arguments.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1891">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1891">Remarks</span></span>

<span data-ttu-id="26fa0-1892">レコードを取得するデータ ソースは、データ ソースに割り当てられたテーブルとオプションのパラメーターによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1892">The data source from which to retrieve the record is specified by the table assigned to the data source and by an optional parameter.</span></span> <span data-ttu-id="26fa0-1893">テーブル (およびオプションのパラメーター) を指定するのではなく、getNo メソッドを使用して、データ ソースの数を引数として取得できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1893">Instead of supplying the table (and optional parameter), you can use the getNo method, which takes the data source number as an argument.</span></span>

### <a name="method-getimpexpdatacontracttype"></a><span data-ttu-id="26fa0-1894">メソッド getImpExpDataContractType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1894">Method getImpExpDataContractType</span></span>

    public System.Type getImpExpDataContractType()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1895">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1895">Return Value</span></span>

### <a name="method-getno"></a><span data-ttu-id="26fa0-1896">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1896">Method getNo</span></span>

<span data-ttu-id="26fa0-1897">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1897">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>

    public Common getNo(int dataSourceNo)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1898">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1898">Parameters</span></span>

<span data-ttu-id="26fa0-1899">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="26fa0-1899">dataSourceNo</span></span>  
<span data-ttu-id="26fa0-1900">現在選択されているレコードを取得する元のデータ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1900">The number of the data source from which to get the currently selected record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="26fa0-1901">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1901">Return Value</span></span>

<span data-ttu-id="26fa0-1902">引数で識別されるデータ ソースのフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1902">Returns the record fetched for the data source identified by the argument.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1903">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1903">Remarks</span></span>

<span data-ttu-id="26fa0-1904">レコードを取り出すデータ ソースは、データ ソースの番号で指定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1904">The data source from which to retrieve the record is specified by the number of the data source.</span></span> <span data-ttu-id="26fa0-1905">データソースは、1 から順にカウントされます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1905">The data sources are counted consecutively, starting from 1.</span></span> <span data-ttu-id="26fa0-1906">代わりに QueryRun.get メソッドを使用できます。このメソッドは、データ ソースを定義するテーブル (およびオプション パラメーター) を使用して指定されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1906">The QueryRun.get Method method can be used instead; that method is supplied with the table (and an optional parameter), that defines the data source.</span></span>

#### <a name="examples"></a><span data-ttu-id="26fa0-1907">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1907">Examples</span></span>

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

### <a name="method-importable"></a><span data-ttu-id="26fa0-1908">メソッド importable</span><span class="sxs-lookup"><span data-stu-id="26fa0-1908">Method importable</span></span>

    public boolean importable()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1909">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1909">Return Value</span></span>

### <a name="method-interactive"></a><span data-ttu-id="26fa0-1910">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="26fa0-1910">Method interactive</span></span>

    public boolean interactive([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1911">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1911">Parameters</span></span>

<span data-ttu-id="26fa0-1912">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1912">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1913">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1913">Return Value</span></span>

### <a name="method-ispositionpagingenabled"></a><span data-ttu-id="26fa0-1914">メソッド isPositionPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="26fa0-1914">Method isPositionPagingEnabled</span></span>

    public boolean isPositionPagingEnabled()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1915">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1915">Return Value</span></span>

### <a name="method-isquerytimedout"></a><span data-ttu-id="26fa0-1916">メソッド isQueryTimedout</span><span class="sxs-lookup"><span data-stu-id="26fa0-1916">Method isQueryTimedout</span></span>

    public boolean isQueryTimedout()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1917">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1917">Return Value</span></span>

### <a name="method-isvaluebasedpagingenabled"></a><span data-ttu-id="26fa0-1918">メソッド isValueBasedPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="26fa0-1918">Method isValueBasedPagingEnabled</span></span>

    public boolean isValueBasedPagingEnabled()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1919">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1919">Return Value</span></span>

### <a name="method-literals"></a><span data-ttu-id="26fa0-1920">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="26fa0-1920">Method literals</span></span>

    public int literals([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1921">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1921">Parameters</span></span>

<span data-ttu-id="26fa0-1922">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1922">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1923">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1923">Return Value</span></span>

### <a name="method-loadcsv"></a><span data-ttu-id="26fa0-1924">メソッド loadCsv</span><span class="sxs-lookup"><span data-stu-id="26fa0-1924">Method loadCsv</span></span>

    public Guid loadCsv(str fileName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1925">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1925">Parameters</span></span>

<span data-ttu-id="26fa0-1926">fileName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1926">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1927">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1927">Return Value</span></span>

### <a name="method-loadxml"></a><span data-ttu-id="26fa0-1928">メソッド loadXml</span><span class="sxs-lookup"><span data-stu-id="26fa0-1928">Method loadXml</span></span>

    public Guid loadXml(str fileName)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1929">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1929">Parameters</span></span>

<span data-ttu-id="26fa0-1930">fileName</span><span class="sxs-lookup"><span data-stu-id="26fa0-1930">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1931">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1931">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="26fa0-1932">メソッド名</span><span class="sxs-lookup"><span data-stu-id="26fa0-1932">Method name</span></span>

<span data-ttu-id="26fa0-1933">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1933">Gets or sets the name that is used in code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1934">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1934">Parameters</span></span>

<span data-ttu-id="26fa0-1935">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1935">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1936">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1936">Return Value</span></span>

<span data-ttu-id="26fa0-1937">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1937">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1938">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1938">Remarks</span></span>

<span data-ttu-id="26fa0-1939">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1939">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="26fa0-1940">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1940">Begins with a letter.</span></span>
-   <span data-ttu-id="26fa0-1941">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1941">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="26fa0-1942">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1942">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="26fa0-1943">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1943">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="26fa0-1944">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1944">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

### <a name="method-newobject"></a><span data-ttu-id="26fa0-1945">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="26fa0-1945">Method newObject</span></span>

    public QueryRun newObject(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="26fa0-1946">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1946">Parameters</span></span>

<span data-ttu-id="26fa0-1947">ソース</span><span class="sxs-lookup"><span data-stu-id="26fa0-1947">source</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1948">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1948">Return Value</span></span>

### <a name="method-next"></a><span data-ttu-id="26fa0-1949">メソッド next</span><span class="sxs-lookup"><span data-stu-id="26fa0-1949">Method next</span></span>

<span data-ttu-id="26fa0-1950">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1950">Retrieves the next record from the query.</span></span>

    public boolean next()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1951">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1951">Return Value</span></span>

<span data-ttu-id="26fa0-1952">次のレコードが利用可能で getNo メソッドまたは get メソッドで取得することができる場合は true。クエリ内に設定された制約を満たすレコードがそれ以上存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1952">true if the next record is available and can be fetched with the getNo method or get method; false if no there are no more records that satisfy the constraint set up in the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1953">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1953">Remarks</span></span>

<span data-ttu-id="26fa0-1954">変更されたメソッドまたは changedNo メソッドを使用して、指定されたデータ ソースのレコードが前回の次のメソッド呼び出しから変更されたかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1954">The changed method or changedNo method can be used to check whether the record from the given data source has changed since the previous call to the next method.</span></span>

#### <a name="examples"></a><span data-ttu-id="26fa0-1955">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1955">Examples</span></span>

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

### <a name="method-nextuniqueid"></a><span data-ttu-id="26fa0-1956">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="26fa0-1956">Method nextUniqueId</span></span>

    public int nextUniqueId([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1957">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1957">Parameters</span></span>

<span data-ttu-id="26fa0-1958">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1958">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1959">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1959">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="26fa0-1960">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="26fa0-1960">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1961">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1961">Parameters</span></span>

<span data-ttu-id="26fa0-1962">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1962">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1963">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1963">Return Value</span></span>

### <a name="method-pack"></a><span data-ttu-id="26fa0-1964">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="26fa0-1964">Method pack</span></span>

    public container pack([boolean doCheck])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1965">Parameters</span></span>

<span data-ttu-id="26fa0-1966">doCheck</span><span class="sxs-lookup"><span data-stu-id="26fa0-1966">doCheck</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1967">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1967">Return Value</span></span>

### <a name="method-prompt"></a><span data-ttu-id="26fa0-1968">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="26fa0-1968">Method prompt</span></span>

<span data-ttu-id="26fa0-1969">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1969">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>

    public boolean prompt()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1970">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1970">Return Value</span></span>

<span data-ttu-id="26fa0-1971">ユーザーが OK をクリックして検索が続行される場合は true。ユーザーがキャンセルをクリックして検索を停止した場合は false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1971">true if the user clicked OK and the search is to continue; false if the user clicked Cancel to stop the search.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-1972">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-1972">Remarks</span></span>

<span data-ttu-id="26fa0-1973">ユーザーには、フェッチされたレコードによって実行される制約を定義する範囲を与えるためのフォームが提示される。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1973">The user is presented with a form to give ranges that define constraints to be fulfilled by the fetched records.</span></span> <span data-ttu-id="26fa0-1974">または、ユーザーは新しいフィールドを追加し、区切ったり、変更したり、並べ替えたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1974">Or the user may add new fields to delimit, change the sorting, and so on.</span></span> <span data-ttu-id="26fa0-1975">このメソッドをオーバーロードすると、事前定義されたクエリ フォームではなく、アプリケーション定義の方法でユーザーにプロンプトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1975">This method can be overloaded to prompt the user in an application-defined way instead of in through the predefined query form.</span></span> <span data-ttu-id="26fa0-1976">または、この方法は、フェッチされるレコードをユーザーがコントロールできないように、オーバーロードされることがあります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1976">Or this method can be overloaded to avoid giving the user control over which records are fetched.</span></span> <span data-ttu-id="26fa0-1977">これらの結果を生成するには、継承したメソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1977">To produce these results, do not call the inherited method.</span></span> <span data-ttu-id="26fa0-1978">いずれの場合でも、関数はクエリが続行する場合は true、それ以外の場合は false を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1978">In any case, the function should return true if the query is to continue, and false otherwise.</span></span>

#### <a name="examples"></a><span data-ttu-id="26fa0-1979">例</span><span class="sxs-lookup"><span data-stu-id="26fa0-1979">Examples</span></span>

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

### <a name="method-query"></a><span data-ttu-id="26fa0-1980">メソッド query</span><span class="sxs-lookup"><span data-stu-id="26fa0-1980">Method query</span></span>

    public Query query([Query query])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1981">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1981">Parameters</span></span>

<span data-ttu-id="26fa0-1982">クエリ</span><span class="sxs-lookup"><span data-stu-id="26fa0-1982">query</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1983">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1983">Return Value</span></span>

### <a name="method-querytype"></a><span data-ttu-id="26fa0-1984">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="26fa0-1984">Method queryType</span></span>

    public int queryType([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1985">Parameters</span></span>

<span data-ttu-id="26fa0-1986">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1986">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1987">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1987">Return Value</span></span>

### <a name="method-recordlevelsecurity"></a><span data-ttu-id="26fa0-1988">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="26fa0-1988">Method recordLevelSecurity</span></span>

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-1989">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-1989">Parameters</span></span>

<span data-ttu-id="26fa0-1990">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1990">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-1991">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1991">Return Value</span></span>

### <a name="method-report"></a><span data-ttu-id="26fa0-1992">メソッド report</span><span class="sxs-lookup"><span data-stu-id="26fa0-1992">Method report</span></span>

    public ReportRun report()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1993">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1993">Return Value</span></span>

### <a name="method-reportrun"></a><span data-ttu-id="26fa0-1994">メソッド reportRun</span><span class="sxs-lookup"><span data-stu-id="26fa0-1994">Method reportRun</span></span>

    public ReportRun reportRun()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1995">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1995">Return Value</span></span>

### <a name="method-saved"></a><span data-ttu-id="26fa0-1996">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="26fa0-1996">Method saved</span></span>

    public boolean saved()

#### <a name="return-value"></a><span data-ttu-id="26fa0-1997">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-1997">Return Value</span></span>

### <a name="method-saveusersetup"></a><span data-ttu-id="26fa0-1998">メソッド saveUserSetup</span><span class="sxs-lookup"><span data-stu-id="26fa0-1998">Method saveUserSetup</span></span>

<span data-ttu-id="26fa0-1999">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-1999">Saves the user setup.</span></span>

    public boolean saveUserSetup([boolean saveIt])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2000">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2000">Parameters</span></span>

<span data-ttu-id="26fa0-2001">saveIt</span><span class="sxs-lookup"><span data-stu-id="26fa0-2001">saveIt</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2002">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2002">Return Value</span></span>

<span data-ttu-id="26fa0-2003">設定が正常に保存された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2003">true if the setup was successfully saved; otherwise false.</span></span>

### <a name="method-searchable"></a><span data-ttu-id="26fa0-2004">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="26fa0-2004">Method searchable</span></span>

    public boolean searchable([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2005">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2005">Parameters</span></span>

<span data-ttu-id="26fa0-2006">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2006">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2007">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2007">Return Value</span></span>

### <a name="method-setcursor"></a><span data-ttu-id="26fa0-2008">メソッド setCursor</span><span class="sxs-lookup"><span data-stu-id="26fa0-2008">Method setCursor</span></span>

    public boolean setCursor(Common record, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2009">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2009">Parameters</span></span>

<span data-ttu-id="26fa0-2010">記録</span><span class="sxs-lookup"><span data-stu-id="26fa0-2010">record</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2011">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-2011">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2012">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2012">Return Value</span></span>

### <a name="method-setrecord"></a><span data-ttu-id="26fa0-2013">メソッド setRecord</span><span class="sxs-lookup"><span data-stu-id="26fa0-2013">Method setRecord</span></span>

    public boolean setRecord(Common record, [int occurrence])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2014">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2014">Parameters</span></span>

<span data-ttu-id="26fa0-2015">記録</span><span class="sxs-lookup"><span data-stu-id="26fa0-2015">record</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2016">occurrence</span><span class="sxs-lookup"><span data-stu-id="26fa0-2016">occurrence</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2017">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2017">Return Value</span></span>

### <a name="method-title"></a><span data-ttu-id="26fa0-2018">メソッド title</span><span class="sxs-lookup"><span data-stu-id="26fa0-2018">Method title</span></span>

    public str title([str value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2019">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2019">Parameters</span></span>

<span data-ttu-id="26fa0-2020">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2020">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2021">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2021">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="26fa0-2022">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="26fa0-2022">Method toString</span></span>

<span data-ttu-id="26fa0-2023">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2023">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="26fa0-2024">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2024">Return Value</span></span>

<span data-ttu-id="26fa0-2025">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2025">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26fa0-2026">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-2026">Remarks</span></span>

<span data-ttu-id="26fa0-2027">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2027">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="26fa0-2028">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2028">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="26fa0-2029">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2029">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-userupdate"></a><span data-ttu-id="26fa0-2030">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="26fa0-2030">Method userUpdate</span></span>

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2031">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2031">Parameters</span></span>

<span data-ttu-id="26fa0-2032">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2032">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2033">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2033">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="26fa0-2034">メソッド version</span><span class="sxs-lookup"><span data-stu-id="26fa0-2034">Method version</span></span>

    public int version([int value])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2035">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2035">Parameters</span></span>

<span data-ttu-id="26fa0-2036">値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2036">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2037">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2037">Return Value</span></span>

### <a name="method-getqueryrowcount"></a><span data-ttu-id="26fa0-2038">メソッド getQueryRowCount</span><span class="sxs-lookup"><span data-stu-id="26fa0-2038">Method getQueryRowCount</span></span>

    public static int getQueryRowCount(Query query, int maxRows)

#### <a name="parameters"></a><span data-ttu-id="26fa0-2039">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2039">Parameters</span></span>

<span data-ttu-id="26fa0-2040">クエリ</span><span class="sxs-lookup"><span data-stu-id="26fa0-2040">query</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2041">maxRows</span><span class="sxs-lookup"><span data-stu-id="26fa0-2041">maxRows</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2042">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2042">Return Value</span></span>

### <a name="method-runandpopulate"></a><span data-ttu-id="26fa0-2043">メソッド runAndPopulate</span><span class="sxs-lookup"><span data-stu-id="26fa0-2043">Method runAndPopulate</span></span>

    public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)

#### <a name="parameters"></a><span data-ttu-id="26fa0-2044">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2044">Parameters</span></span>

<span data-ttu-id="26fa0-2045">sourceRuery</span><span class="sxs-lookup"><span data-stu-id="26fa0-2045">sourceRuery</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2046">targetTable</span><span class="sxs-lookup"><span data-stu-id="26fa0-2046">targetTable</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2047">queryAliasesAndTargetColumnsMap</span><span class="sxs-lookup"><span data-stu-id="26fa0-2047">queryAliasesAndTargetColumnsMap</span></span>  

#### <a name="return-value"></a><span data-ttu-id="26fa0-2048">戻り値</span><span class="sxs-lookup"><span data-stu-id="26fa0-2048">Return Value</span></span>

### <a name="method-run"></a><span data-ttu-id="26fa0-2049">メソッド run</span><span class="sxs-lookup"><span data-stu-id="26fa0-2049">Method run</span></span>

<span data-ttu-id="26fa0-2050">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2050">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>

    public void run()

#### <a name="remarks"></a><span data-ttu-id="26fa0-2051">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-2051">Remarks</span></span>

<span data-ttu-id="26fa0-2052">クエリを実行すると、ユーザーによって入力された制約を満たすレコードが検索されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2052">Running the query will find the records that satisfy the constraints entered by the user.</span></span> <span data-ttu-id="26fa0-2053">ただし、この方法でのクエリの実行には副作用がありません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2053">However, running the query in this manner has no side effects.</span></span> <span data-ttu-id="26fa0-2054">扱いやすくするために、1 つ以上の継承されたメソッドをオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2054">In order to be useful, one or more of the inherited methods must be overloaded.</span></span>

### <a name="method-new"></a><span data-ttu-id="26fa0-2055">メソッド new</span><span class="sxs-lookup"><span data-stu-id="26fa0-2055">Method new</span></span>

<span data-ttu-id="26fa0-2056">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2056">Initializes a new instance of the Object class.</span></span>

    public void new(AnyType source)

#### <a name="parameters"></a><span data-ttu-id="26fa0-2057">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2057">Parameters</span></span>

<span data-ttu-id="26fa0-2058">ソース</span><span class="sxs-lookup"><span data-stu-id="26fa0-2058">source</span></span>  

#### <a name="remarks"></a><span data-ttu-id="26fa0-2059">備考</span><span class="sxs-lookup"><span data-stu-id="26fa0-2059">Remarks</span></span>

<span data-ttu-id="26fa0-2060">クエリ クラスのインスタンスを QueryRun クラスのコンストラクターに渡すと、クエリ オブジェクトのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2060">When you pass an instance of the Query class into this constructor of the QueryRun class, a copy of the Query object is created.</span></span> <span data-ttu-id="26fa0-2061">このクエリ オブジェクト のコピーに加えられた変更は、元のクエリ オブジェクトには影響しません。</span><span class="sxs-lookup"><span data-stu-id="26fa0-2061">Changes that are made to this copy of the Query object do not affect the original Query object.</span></span>

### <a name="method-addpagerange"></a><span data-ttu-id="26fa0-2062">メソッド addPageRange</span><span class="sxs-lookup"><span data-stu-id="26fa0-2062">Method addPageRange</span></span>

    public void addPageRange([Int64 startingPosition], [Int64 numberOfRecordsToFetch])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2063">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2063">Parameters</span></span>

<span data-ttu-id="26fa0-2064">startingPosition</span><span class="sxs-lookup"><span data-stu-id="26fa0-2064">startingPosition</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2065">numberOfRecordsToFetch</span><span class="sxs-lookup"><span data-stu-id="26fa0-2065">numberOfRecordsToFetch</span></span>  

### <a name="method-reset"></a><span data-ttu-id="26fa0-2066">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="26fa0-2066">Method reset</span></span>

    public void reset()

### <a name="method-setimportsession"></a><span data-ttu-id="26fa0-2067">メソッド setImportSession</span><span class="sxs-lookup"><span data-stu-id="26fa0-2067">Method setImportSession</span></span>

    public void setImportSession(Guid importSession)

#### <a name="parameters"></a><span data-ttu-id="26fa0-2068">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2068">Parameters</span></span>

<span data-ttu-id="26fa0-2069">importSession</span><span class="sxs-lookup"><span data-stu-id="26fa0-2069">importSession</span></span>  

### <a name="method-setquerytimeout"></a><span data-ttu-id="26fa0-2070">メソッド setQuerytimeout</span><span class="sxs-lookup"><span data-stu-id="26fa0-2070">Method setQuerytimeout</span></span>

    public void setQuerytimeout(int seconds, [boolean raiseException])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2071">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2071">Parameters</span></span>

<span data-ttu-id="26fa0-2072"> 秒</span><span class="sxs-lookup"><span data-stu-id="26fa0-2072">seconds</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2073">raiseException</span><span class="sxs-lookup"><span data-stu-id="26fa0-2073">raiseException</span></span>  

### <a name="method-init"></a><span data-ttu-id="26fa0-2074">メソッド init</span><span class="sxs-lookup"><span data-stu-id="26fa0-2074">Method init</span></span>

    public void init()

### <a name="method-enablepositionpaging"></a><span data-ttu-id="26fa0-2075">メソッド enablePositionPaging</span><span class="sxs-lookup"><span data-stu-id="26fa0-2075">Method enablePositionPaging</span></span>

    public void enablePositionPaging([boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2076">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2076">Parameters</span></span>

<span data-ttu-id="26fa0-2077">有効</span><span class="sxs-lookup"><span data-stu-id="26fa0-2077">enabled</span></span>  

### <a name="method-shred"></a><span data-ttu-id="26fa0-2078">メソッド shred</span><span class="sxs-lookup"><span data-stu-id="26fa0-2078">Method shred</span></span>

    public void shred(Guid importSession)

#### <a name="parameters"></a><span data-ttu-id="26fa0-2079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2079">Parameters</span></span>

<span data-ttu-id="26fa0-2080">importSession</span><span class="sxs-lookup"><span data-stu-id="26fa0-2080">importSession</span></span>  

### <a name="method-enablevaluebasedpaging"></a><span data-ttu-id="26fa0-2081">メソッド enableValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="26fa0-2081">Method enableValueBasedPaging</span></span>

    public void enableValueBasedPaging([boolean enable])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2082">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2082">Parameters</span></span>

<span data-ttu-id="26fa0-2083">enable</span><span class="sxs-lookup"><span data-stu-id="26fa0-2083">enable</span></span>  

### <a name="method-bulknext"></a><span data-ttu-id="26fa0-2084">メソッド bulkNext</span><span class="sxs-lookup"><span data-stu-id="26fa0-2084">Method bulkNext</span></span>

    public void bulkNext([boolean fetchAllData])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2085">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2085">Parameters</span></span>

<span data-ttu-id="26fa0-2086">fetchAllData</span><span class="sxs-lookup"><span data-stu-id="26fa0-2086">fetchAllData</span></span>  

### <a name="method-applyvaluebasedpaging"></a><span data-ttu-id="26fa0-2087">メソッド applyValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="26fa0-2087">Method applyValueBasedPaging</span></span>

    public void applyValueBasedPaging([Common sourceCursor], [boolean isForward])

#### <a name="parameters"></a><span data-ttu-id="26fa0-2088">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26fa0-2088">Parameters</span></span>

<span data-ttu-id="26fa0-2089">sourceCursor</span><span class="sxs-lookup"><span data-stu-id="26fa0-2089">sourceCursor</span></span>  

<!-- -->

<span data-ttu-id="26fa0-2090">isForward</span><span class="sxs-lookup"><span data-stu-id="26fa0-2090">isForward</span></span>  





