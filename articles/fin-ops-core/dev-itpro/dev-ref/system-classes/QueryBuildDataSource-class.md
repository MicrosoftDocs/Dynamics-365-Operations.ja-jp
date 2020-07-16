---
title: QueryBuildDataSource クラス
description: このトピックでは、QueryBuildDataSource クラスについて説明します。
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
ms.openlocfilehash: 95f9d1cfdd34a20ed595ad6009ef8491d753a05b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502869"
---
# <a name="class-querybuilddatasource"></a><span data-ttu-id="282d4-103">クラス QueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-103">Class QueryBuildDataSource</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildDataSource extends TreeNode
```

<span data-ttu-id="282d4-104">QueryBuildDataSource クラスは、クエリが構成されているレポート パーツを提供します。</span><span class="sxs-lookup"><span data-stu-id="282d4-104">The QueryBuildDataSource class provides the building blocks that queries are made of.</span></span>

## <a name="remarks"></a><span data-ttu-id="282d4-105">備考</span><span class="sxs-lookup"><span data-stu-id="282d4-105">Remarks</span></span>

<span data-ttu-id="282d4-106">データ ソースは、データ ソースに割り当てられたテーブルからレコードがフェッチされる順序を定義する階層内で配置されます。</span><span class="sxs-lookup"><span data-stu-id="282d4-106">Data sources are arranged in hierarchies that define the sequence in which records are fetched from the tables that are assigned to the data sources.</span></span> <span data-ttu-id="282d4-107">各データ ソースでは、レコードがフェッチされる順序および選択されたレコードによって満たされなければならない基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="282d4-107">Each data source defines the order in which the records are fetched, and also the criteria that must be met by the selected records.</span></span> <span data-ttu-id="282d4-108">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="282d4-108">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="282d4-109">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="282d4-109">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="282d4-110">例</span><span class="sxs-lookup"><span data-stu-id="282d4-110">Examples</span></span>

```xpp
{    QueryBuildDataSource ds;    Query q = new Query();        ds = q.addDataSource(        TableNum(CustTable));}
```

## <a name="methods"></a><span data-ttu-id="282d4-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="282d4-111">Methods</span></span>

| <span data-ttu-id="282d4-112">方法</span><span class="sxs-lookup"><span data-stu-id="282d4-112">Method</span></span>                                                                                                                                                       | <span data-ttu-id="282d4-113">説明</span><span class="sxs-lookup"><span data-stu-id="282d4-113">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="282d4-114">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="282d4-114">public int addAllFields(TableName tableName)</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="282d4-115">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span><span class="sxs-lookup"><span data-stu-id="282d4-115">public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])</span></span>                                                             | <span data-ttu-id="282d4-116">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="282d4-116">Adds a data source that is embedded in this data source.</span></span>                                                                                  |
| <span data-ttu-id="282d4-117">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-117">public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])</span></span>      |                                                                                                                                           |
| <span data-ttu-id="282d4-118">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="282d4-118">public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="282d4-119">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-119">public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="282d4-120">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="282d4-120">public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-121">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-121">public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="282d4-122">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="282d4-122">public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="282d4-123">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-123">public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-124">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span><span class="sxs-lookup"><span data-stu-id="282d4-124">public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])</span></span>                                                             | <span data-ttu-id="282d4-125">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="282d4-125">Adds a range to the data source.</span></span>                                                                                                          |
| <span data-ttu-id="282d4-126">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-126">public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-127">public int addSortIndex(IndexId index)</span><span class="sxs-lookup"><span data-stu-id="282d4-127">public int addSortIndex(IndexId index)</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-128">public int allowAdd(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-128">public int allowAdd(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="282d4-129">public boolean applyFilter(FilterValue filterValue)</span><span class="sxs-lookup"><span data-stu-id="282d4-129">public boolean applyFilter(FilterValue filterValue)</span></span>                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-130">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="282d4-130">public boolean autoHeader(FieldId field, \[boolean orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="282d4-131">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="282d4-131">public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="282d4-132">public boolean autoSum(FieldId field, \[boolean orderNo\])</span><span class="sxs-lookup"><span data-stu-id="282d4-132">public boolean autoSum(FieldId field, \[boolean orderNo\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-133">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span><span class="sxs-lookup"><span data-stu-id="282d4-133">public int autoSumDetailLevel(FieldId field, \[int orderNo\])</span></span>                                                                                                |                                                                                                                                           |
| <span data-ttu-id="282d4-134">public boolean changedNo()</span><span class="sxs-lookup"><span data-stu-id="282d4-134">public boolean changedNo()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-135">public int childDataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-135">public int childDataSourceCount()</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="282d4-136">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-136">public QueryBuildDataSource childDataSourceNo(int dataSourceNo)</span></span>                                                                                              |                                                                                                                                           |
| <span data-ttu-id="282d4-137">public str company(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-137">public str company(\[str value\])</span></span>                                                                                                                            |                                                                                                                                           |
| <span data-ttu-id="282d4-138">public int concurrencyModel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-138">public int concurrencyModel(\[int value\])</span></span>                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-139">public QueryBuildDynalink dynalink(int dynalinkNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-139">public QueryBuildDynalink dynalink(int dynalinkNo)</span></span>                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="282d4-140">public int dynalinkCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-140">public int dynalinkCount()</span></span>                                                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-141">public boolean embedded()</span><span class="sxs-lookup"><span data-stu-id="282d4-141">public boolean embedded()</span></span>                                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="282d4-142">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-142">public boolean enabled(\[boolean value\])</span></span>                                                                                                                    | <span data-ttu-id="282d4-143">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-143">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="282d4-144">public boolean existsMeanOrExists(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-144">public boolean existsMeanOrExists(\[boolean value\])</span></span>                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="282d4-145">public int fetchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-145">public int fetchMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-146">public QueryBuildFieldList fields()</span><span class="sxs-lookup"><span data-stu-id="282d4-146">public QueryBuildFieldList fields()</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-147">public TableId file()</span><span class="sxs-lookup"><span data-stu-id="282d4-147">public TableId file()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="282d4-148">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-148">public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-149">public boolean firstFast(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-149">public boolean firstFast(\[boolean value\])</span></span>                                                                                                                  | <span data-ttu-id="282d4-150">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-150">Determines whether to retrieve the first record from the query before the other records.</span></span>                                                  |
| <span data-ttu-id="282d4-151">public boolean firstOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-151">public boolean firstOnly(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="282d4-152">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-152">public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="282d4-153">public Common getNo()</span><span class="sxs-lookup"><span data-stu-id="282d4-153">public Common getNo()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="282d4-154">public int id()</span><span class="sxs-lookup"><span data-stu-id="282d4-154">public int id()</span></span>                                                                                                                                              |                                                                                                                                           |
| <span data-ttu-id="282d4-155">public boolean indexIsHint(boolean arg)</span><span class="sxs-lookup"><span data-stu-id="282d4-155">public boolean indexIsHint(boolean arg)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-156">public boolean isPartOfSubQueryInBaseQuery()</span><span class="sxs-lookup"><span data-stu-id="282d4-156">public boolean isPartOfSubQueryInBaseQuery()</span></span>                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="282d4-157">public boolean joined()</span><span class="sxs-lookup"><span data-stu-id="282d4-157">public boolean joined()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-158">public container joinedDataSources()</span><span class="sxs-lookup"><span data-stu-id="282d4-158">public container joinedDataSources()</span></span>                                                                                                                         |                                                                                                                                           |
| <span data-ttu-id="282d4-159">public int joinMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-159">public int joinMode(\[int value\])</span></span>                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="282d4-160">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-160">public str label(\[str value\])</span></span>                                                                                                                              | <span data-ttu-id="282d4-161">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-161">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="282d4-162">public int level()</span><span class="sxs-lookup"><span data-stu-id="282d4-162">public int level()</span></span>                                                                                                                                           |                                                                                                                                           |
| <span data-ttu-id="282d4-163">public QueryBuildLink link(int associationNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-163">public QueryBuildLink link(int associationNo)</span></span>                                                                                                                |                                                                                                                                           |
| <span data-ttu-id="282d4-164">public int linkCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-164">public int linkCount()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-165">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-165">public str name(\[str value\])</span></span>                                                                                                                               | <span data-ttu-id="282d4-166">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-166">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="282d4-167">public container oneToOneDataSources()</span><span class="sxs-lookup"><span data-stu-id="282d4-167">public container oneToOneDataSources()</span></span>                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-168">public int orderMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-168">public int orderMode(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-169">public QueryBuildDataSource parentDataSource()</span><span class="sxs-lookup"><span data-stu-id="282d4-169">public QueryBuildDataSource parentDataSource()</span></span>                                                                                                               |                                                                                                                                           |
| <span data-ttu-id="282d4-170">public str policyContext(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-170">public str policyContext(\[str value\])</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-171">public QueryBuildRange range(int rangeNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-171">public QueryBuildRange range(int rangeNo)</span></span>                                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="282d4-172">public int rangeCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-172">public int rangeCount()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-173">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="282d4-173">public QueryBuildRange rangeField(FieldId field, \[int occurrence\])</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="282d4-174">public boolean relations(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-174">public boolean relations(\[boolean value\])</span></span>                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="282d4-175">public int selectionCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-175">public int selectionCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="282d4-176">public boolean selectWithRepeatableRead(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-176">public boolean selectWithRepeatableRead(\[boolean value\])</span></span>                                                                                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-177">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span><span class="sxs-lookup"><span data-stu-id="282d4-177">public SortOrder sortDirection(FieldId field, \[SortOrder direction\])</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-178">public FieldId sortField(FieldId field)</span><span class="sxs-lookup"><span data-stu-id="282d4-178">public FieldId sortField(FieldId field)</span></span>                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-179">public int sortFieldCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-179">public int sortFieldCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="282d4-180">public IndexId sortIndex(int indexNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-180">public IndexId sortIndex(int indexNo)</span></span>                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="282d4-181">public int sortIndexCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-181">public int sortIndexCount()</span></span>                                                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="282d4-182">public QueryBuildStaticlink staticlink(int staticlinkNo)</span><span class="sxs-lookup"><span data-stu-id="282d4-182">public QueryBuildStaticlink staticlink(int staticlinkNo)</span></span>                                                                                                     | <span data-ttu-id="282d4-183">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-183">Returns a static Link object on the query�s data source.</span></span>                                                                                  |
| <span data-ttu-id="282d4-184">public int staticlinkCount()</span><span class="sxs-lookup"><span data-stu-id="282d4-184">public int staticlinkCount()</span></span>                                                                                                                                 | <span data-ttu-id="282d4-185">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="282d4-185">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>                                                     |
| <span data-ttu-id="282d4-186">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-186">public TableId table(\[TableId value\])</span></span>                                                                                                                      | <span data-ttu-id="282d4-187">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-187">Gets or sets the table ID that is associated with the object.</span></span>                                                                             |
| <span data-ttu-id="282d4-188">public str toString()</span><span class="sxs-lookup"><span data-stu-id="282d4-188">public str toString()</span></span>                                                                                                                                        | <span data-ttu-id="282d4-189">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-189">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="282d4-190">public int unionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-190">public int unionType(\[int value\])</span></span>                                                                                                                          |                                                                                                                                           |
| <span data-ttu-id="282d4-191">public int uniqueId()</span><span class="sxs-lookup"><span data-stu-id="282d4-191">public int uniqueId()</span></span>                                                                                                                                        |                                                                                                                                           |
| <span data-ttu-id="282d4-192">public boolean update(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="282d4-192">public boolean update(\[boolean value\])</span></span>                                                                                                                     | <span data-ttu-id="282d4-193">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-193">Determines whether the records fetched by this data source can be updated.</span></span>                                                                |
| <span data-ttu-id="282d4-194">public void clearLinks()</span><span class="sxs-lookup"><span data-stu-id="282d4-194">public void clearLinks()</span></span>                                                                                                                                     |                                                                                                                                           |
| <span data-ttu-id="282d4-195">public void clearDynalinks()</span><span class="sxs-lookup"><span data-stu-id="282d4-195">public void clearDynalinks()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="282d4-196">public void clearRange(FieldId field, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="282d4-196">public void clearRange(FieldId field, \[int occurrence\])</span></span>                                                                                                    |                                                                                                                                           |
| <span data-ttu-id="282d4-197">public void sortClear()</span><span class="sxs-lookup"><span data-stu-id="282d4-197">public void sortClear()</span></span>                                                                                                                                      |                                                                                                                                           |
| <span data-ttu-id="282d4-198">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="282d4-198">public void finalize()</span></span>                                                                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-199">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span><span class="sxs-lookup"><span data-stu-id="282d4-199">public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="282d4-200">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span><span class="sxs-lookup"><span data-stu-id="282d4-200">public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="282d4-201">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span><span class="sxs-lookup"><span data-stu-id="282d4-201">public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)</span></span>                                                                                       |                                                                                                                                           |
| <span data-ttu-id="282d4-202">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span><span class="sxs-lookup"><span data-stu-id="282d4-202">public void addRelation(DictRelation relation, \[TableScope tableScope\])</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="282d4-203">public void clearSortIndex()</span><span class="sxs-lookup"><span data-stu-id="282d4-203">public void clearSortIndex()</span></span>                                                                                                                                 |                                                                                                                                           |
| <span data-ttu-id="282d4-204">public void clearRanges()</span><span class="sxs-lookup"><span data-stu-id="282d4-204">public void clearRanges()</span></span>                                                                                                                                    | <span data-ttu-id="282d4-205">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="282d4-205">Deletes all ranges that are associated with the data source.</span></span>                                                                              |
| <span data-ttu-id="282d4-206">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span><span class="sxs-lookup"><span data-stu-id="282d4-206">public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="282d4-207">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="282d4-207">public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])</span></span>                                                               |                                                                                                                                           |

## <a name="method-addallfields"></a><span data-ttu-id="282d4-208">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="282d4-208">Method addAllFields</span></span>

```xpp
public int addAllFields(TableName tableName)
```

### <a name="parameters---addallfields"></a><span data-ttu-id="282d4-209">パラメーター - addAllFields</span><span class="sxs-lookup"><span data-stu-id="282d4-209">Parameters - addAllFields</span></span>

<span data-ttu-id="282d4-210">tableName</span><span class="sxs-lookup"><span data-stu-id="282d4-210">tableName</span></span>  

### <a name="return-value---addallfields"></a><span data-ttu-id="282d4-211">戻り値 - addAllFields</span><span class="sxs-lookup"><span data-stu-id="282d4-211">Return Value - addAllFields</span></span>

## <a name="method-adddatasource"></a><span data-ttu-id="282d4-212">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-212">Method addDataSource</span></span>

<span data-ttu-id="282d4-213">このデータ ソースに埋め込まれているデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="282d4-213">Adds a data source that is embedded in this data source.</span></span>

```xpp
public QueryBuildDataSource addDataSource(AnyType arg, [str name], [boolean emptyFieldList])
```

### <a name="parameters---adddatasource"></a><span data-ttu-id="282d4-214">パラメーター - addDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-214">Parameters - addDataSource</span></span>

<span data-ttu-id="282d4-215">arg</span><span class="sxs-lookup"><span data-stu-id="282d4-215">arg</span></span>  

<!-- -->

<span data-ttu-id="282d4-216">名前</span><span class="sxs-lookup"><span data-stu-id="282d4-216">name</span></span>  

<!-- -->

<span data-ttu-id="282d4-217">emptyFieldList</span><span class="sxs-lookup"><span data-stu-id="282d4-217">emptyFieldList</span></span>  

### <a name="return-value---adddatasource"></a><span data-ttu-id="282d4-218">戻り値 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-218">Return Value - addDataSource</span></span>

<span data-ttu-id="282d4-219">新しいデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="282d4-219">The new data source.</span></span>

### <a name="remarks---adddatasource"></a><span data-ttu-id="282d4-220">備考 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-220">Remarks - addDataSource</span></span>

<span data-ttu-id="282d4-221">最上位レベルのデータ ソースは、addDataSource メソッドを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="282d4-221">Top-level data sources are created by using the addDataSource method.</span></span>

## <a name="method-adddynalink"></a><span data-ttu-id="282d4-222">メソッド addDynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-222">Method addDynalink</span></span>

```xpp
public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, [int fieldArrayIndex], [int dynamicFieldArrayIndex])
```

### <a name="parameters---adddynalink"></a><span data-ttu-id="282d4-223">パラメーター - addDynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-223">Parameters - addDynalink</span></span>

<span data-ttu-id="282d4-224"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-224">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-225">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="282d4-225">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="282d4-226">dynamicField</span><span class="sxs-lookup"><span data-stu-id="282d4-226">dynamicField</span></span>  

<!-- -->

<span data-ttu-id="282d4-227">fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-227">fieldArrayIndex</span></span>  

<!-- -->

<span data-ttu-id="282d4-228">dynamicFieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-228">dynamicFieldArrayIndex</span></span>  

### <a name="return-value---adddynalink"></a><span data-ttu-id="282d4-229">戻り値 - addDynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-229">Return Value - addDynalink</span></span>

## <a name="method-addforeignkeyrelation"></a><span data-ttu-id="282d4-230">メソッド addForeignkeyRelation</span><span class="sxs-lookup"><span data-stu-id="282d4-230">Method addForeignkeyRelation</span></span>

```xpp
public QueryBuildLink addForeignkeyRelation(str relatedTableRole, [str parentDatasourceName])
```

### <a name="parameters---addforeignkeyrelation"></a><span data-ttu-id="282d4-231">パラメーター - addForeignkeyRelation</span><span class="sxs-lookup"><span data-stu-id="282d4-231">Parameters - addForeignkeyRelation</span></span>

<span data-ttu-id="282d4-232">relatedTableRole</span><span class="sxs-lookup"><span data-stu-id="282d4-232">relatedTableRole</span></span>  

<!-- -->

<span data-ttu-id="282d4-233">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="282d4-233">parentDatasourceName</span></span>  

### <a name="return-value---addforeignkeyrelation"></a><span data-ttu-id="282d4-234">戻り値 - addForeignkeyRelation</span><span class="sxs-lookup"><span data-stu-id="282d4-234">Return Value - addForeignkeyRelation</span></span>

## <a name="method-addgroupbyfield"></a><span data-ttu-id="282d4-235">メソッド addGroupByField</span><span class="sxs-lookup"><span data-stu-id="282d4-235">Method addGroupByField</span></span>

```xpp
public QueryGroupByField addGroupByField(FieldId fieldID, [int arrayIndex])
```

### <a name="parameters---addgroupbyfield"></a><span data-ttu-id="282d4-236">パラメーター - addGroupByField</span><span class="sxs-lookup"><span data-stu-id="282d4-236">Parameters - addGroupByField</span></span>

<span data-ttu-id="282d4-237">fieldID</span><span class="sxs-lookup"><span data-stu-id="282d4-237">fieldID</span></span>  

<!-- -->

<span data-ttu-id="282d4-238">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-238">arrayIndex</span></span>  

### <a name="return-value---addgroupbyfield"></a><span data-ttu-id="282d4-239">戻り値 - addGroupByField</span><span class="sxs-lookup"><span data-stu-id="282d4-239">Return Value - addGroupByField</span></span>

## <a name="method-addlink"></a><span data-ttu-id="282d4-240">メソッド addLink</span><span class="sxs-lookup"><span data-stu-id="282d4-240">Method addLink</span></span>

```xpp
public QueryBuildLink addLink(FieldId parentField, FieldId thisField, [str parentDatasourceName])
```

### <a name="parameters---addlink"></a><span data-ttu-id="282d4-241">パラメーター - addLink</span><span class="sxs-lookup"><span data-stu-id="282d4-241">Parameters - addLink</span></span>

<span data-ttu-id="282d4-242">parentField</span><span class="sxs-lookup"><span data-stu-id="282d4-242">parentField</span></span>  

<!-- -->

<span data-ttu-id="282d4-243">thisField</span><span class="sxs-lookup"><span data-stu-id="282d4-243">thisField</span></span>  

<!-- -->

<span data-ttu-id="282d4-244">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="282d4-244">parentDatasourceName</span></span>  

### <a name="return-value---addlink"></a><span data-ttu-id="282d4-245">戻り値 - addLink</span><span class="sxs-lookup"><span data-stu-id="282d4-245">Return Value - addLink</span></span>

## <a name="method-addorderbyaggregatefield"></a><span data-ttu-id="282d4-246">メソッド addOrderByAggregateField</span><span class="sxs-lookup"><span data-stu-id="282d4-246">Method addOrderByAggregateField</span></span>

```xpp
public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addorderbyaggregatefield"></a><span data-ttu-id="282d4-247">パラメーター - addOrderByAggregateField</span><span class="sxs-lookup"><span data-stu-id="282d4-247">Parameters - addOrderByAggregateField</span></span>

<span data-ttu-id="282d4-248">fieldType</span><span class="sxs-lookup"><span data-stu-id="282d4-248">fieldType</span></span>  

<!-- -->

<span data-ttu-id="282d4-249">fieldID</span><span class="sxs-lookup"><span data-stu-id="282d4-249">fieldID</span></span>  

<!-- -->

<span data-ttu-id="282d4-250">direction</span><span class="sxs-lookup"><span data-stu-id="282d4-250">direction</span></span>  

<!-- -->

<span data-ttu-id="282d4-251">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-251">arrayIndex</span></span>  

### <a name="return-value---addorderbyaggregatefield"></a><span data-ttu-id="282d4-252">戻り値 - addOrderByAggregateField</span><span class="sxs-lookup"><span data-stu-id="282d4-252">Return Value - addOrderByAggregateField</span></span>

## <a name="method-addorderbycalculationfield"></a><span data-ttu-id="282d4-253">メソッド addOrderByCalculationField</span><span class="sxs-lookup"><span data-stu-id="282d4-253">Method addOrderByCalculationField</span></span>

```xpp
public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, [SortOrder direction])
```

### <a name="parameters---addorderbycalculationfield"></a><span data-ttu-id="282d4-254">パラメーター - addOrderByCalculationField</span><span class="sxs-lookup"><span data-stu-id="282d4-254">Parameters - addOrderByCalculationField</span></span>

<span data-ttu-id="282d4-255">計算</span><span class="sxs-lookup"><span data-stu-id="282d4-255">calculation</span></span>  

<!-- -->

<span data-ttu-id="282d4-256">direction</span><span class="sxs-lookup"><span data-stu-id="282d4-256">direction</span></span>  

### <a name="return-value---addorderbycalculationfield"></a><span data-ttu-id="282d4-257">戻り値 - addOrderByCalculationField</span><span class="sxs-lookup"><span data-stu-id="282d4-257">Return Value - addOrderByCalculationField</span></span>

## <a name="method-addorderbyfield"></a><span data-ttu-id="282d4-258">メソッド addOrderByField</span><span class="sxs-lookup"><span data-stu-id="282d4-258">Method addOrderByField</span></span>

```xpp
public QueryOrderByField addOrderByField(FieldId fieldID, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addorderbyfield"></a><span data-ttu-id="282d4-259">パラメーター - addOrderByField</span><span class="sxs-lookup"><span data-stu-id="282d4-259">Parameters - addOrderByField</span></span>

<span data-ttu-id="282d4-260">fieldID</span><span class="sxs-lookup"><span data-stu-id="282d4-260">fieldID</span></span>  

<!-- -->

<span data-ttu-id="282d4-261">direction</span><span class="sxs-lookup"><span data-stu-id="282d4-261">direction</span></span>  

<!-- -->

<span data-ttu-id="282d4-262">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-262">arrayIndex</span></span>  

### <a name="return-value---addorderbyfield"></a><span data-ttu-id="282d4-263">戻り値 - addOrderByField</span><span class="sxs-lookup"><span data-stu-id="282d4-263">Return Value - addOrderByField</span></span>

## <a name="method-addrange"></a><span data-ttu-id="282d4-264">メソッド addRange</span><span class="sxs-lookup"><span data-stu-id="282d4-264">Method addRange</span></span>

<span data-ttu-id="282d4-265">データ ソースに範囲を追加します。</span><span class="sxs-lookup"><span data-stu-id="282d4-265">Adds a range to the data source.</span></span>

```xpp
public QueryBuildRange addRange(FieldId field, [int arrayIndex], [QueryRangeType rangeType])
```

### <a name="parameters---addrange"></a><span data-ttu-id="282d4-266">パラメーター - addRange</span><span class="sxs-lookup"><span data-stu-id="282d4-266">Parameters - addRange</span></span>

<span data-ttu-id="282d4-267"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-267">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-268">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-268">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="282d4-269">rangeType</span><span class="sxs-lookup"><span data-stu-id="282d4-269">rangeType</span></span>  

### <a name="return-value---addrange"></a><span data-ttu-id="282d4-270">戻り値 - addRange</span><span class="sxs-lookup"><span data-stu-id="282d4-270">Return Value - addRange</span></span>

<span data-ttu-id="282d4-271">データ ソースの新しい範囲。</span><span class="sxs-lookup"><span data-stu-id="282d4-271">A new range for the data source.</span></span>

### <a name="remarks---addrange"></a><span data-ttu-id="282d4-272">備考 - addRange</span><span class="sxs-lookup"><span data-stu-id="282d4-272">Remarks - addRange</span></span>

<span data-ttu-id="282d4-273">範囲は、データ ソースのテーブルのレコードが満たす必要がある値を定義します。</span><span class="sxs-lookup"><span data-stu-id="282d4-273">Ranges define the values that records from the data source's table must satisfy.</span></span> <span data-ttu-id="282d4-274">いくつかの値の範囲は、特定のデータ ソース内の同じフィールドに存在することができます。</span><span class="sxs-lookup"><span data-stu-id="282d4-274">Several range values can exist for the same field in a particular data source.</span></span> <span data-ttu-id="282d4-275">この場合、レコードが提供される値のいずれかにが適用される場合、値はクエリに含まれます。</span><span class="sxs-lookup"><span data-stu-id="282d4-275">In this case, the values are included in the query if the record qualifies for any of the values that are supplied.</span></span> <span data-ttu-id="282d4-276">複数のフィールドの範囲が含まれているときは、両方の条件によって提供される制約を満たすレコードだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="282d4-276">When ranges are included for multiple fields, only records that satisfy the constraints that are supplied by both criteria are included.</span></span> <span data-ttu-id="282d4-277">制約は値のメソッドで指定されます。</span><span class="sxs-lookup"><span data-stu-id="282d4-277">The constraints are specified in the value method.</span></span>

## <a name="method-addsortfield"></a><span data-ttu-id="282d4-278">メソッド addSortField</span><span class="sxs-lookup"><span data-stu-id="282d4-278">Method addSortField</span></span>

```xpp
public int addSortField(FieldId sortField, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addsortfield"></a><span data-ttu-id="282d4-279">パラメーター - addSortField</span><span class="sxs-lookup"><span data-stu-id="282d4-279">Parameters - addSortField</span></span>

<span data-ttu-id="282d4-280">sortField</span><span class="sxs-lookup"><span data-stu-id="282d4-280">sortField</span></span>  

<!-- -->

<span data-ttu-id="282d4-281">direction</span><span class="sxs-lookup"><span data-stu-id="282d4-281">direction</span></span>  

<!-- -->

<span data-ttu-id="282d4-282">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-282">arrayIndex</span></span>  

### <a name="return-value---addsortfield"></a><span data-ttu-id="282d4-283">戻り値 - addSortField</span><span class="sxs-lookup"><span data-stu-id="282d4-283">Return Value - addSortField</span></span>

## <a name="method-addsortindex"></a><span data-ttu-id="282d4-284">メソッド addSortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-284">Method addSortIndex</span></span>

```xpp
public int addSortIndex(IndexId index)
```

### <a name="parameters---addsortindex"></a><span data-ttu-id="282d4-285">パラメーター - addSortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-285">Parameters - addSortIndex</span></span>

<span data-ttu-id="282d4-286">指数</span><span class="sxs-lookup"><span data-stu-id="282d4-286">index</span></span>  

### <a name="return-value---addsortindex"></a><span data-ttu-id="282d4-287">戻り値 - addSortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-287">Return Value - addSortIndex</span></span>

## <a name="method-allowadd"></a><span data-ttu-id="282d4-288">メソッド allowAdd</span><span class="sxs-lookup"><span data-stu-id="282d4-288">Method allowAdd</span></span>

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a><span data-ttu-id="282d4-289">パラメーター - allowAdd</span><span class="sxs-lookup"><span data-stu-id="282d4-289">Parameters - allowAdd</span></span>

<span data-ttu-id="282d4-290">値</span><span class="sxs-lookup"><span data-stu-id="282d4-290">value</span></span>  

### <a name="return-value---allowadd"></a><span data-ttu-id="282d4-291">戻り値 - allowAdd</span><span class="sxs-lookup"><span data-stu-id="282d4-291">Return Value - allowAdd</span></span>

## <a name="method-applyfilter"></a><span data-ttu-id="282d4-292">メソッド applyFilter</span><span class="sxs-lookup"><span data-stu-id="282d4-292">Method applyFilter</span></span>

```xpp
public boolean applyFilter(FilterValue filterValue)
```

### <a name="parameters---applyfilter"></a><span data-ttu-id="282d4-293">パラメーター - applyFilter</span><span class="sxs-lookup"><span data-stu-id="282d4-293">Parameters - applyFilter</span></span>

<span data-ttu-id="282d4-294">filterValue</span><span class="sxs-lookup"><span data-stu-id="282d4-294">filterValue</span></span>  

### <a name="return-value---applyfilter"></a><span data-ttu-id="282d4-295">戻り値 - applyFilter</span><span class="sxs-lookup"><span data-stu-id="282d4-295">Return Value - applyFilter</span></span>

## <a name="method-autoheader"></a><span data-ttu-id="282d4-296">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="282d4-296">Method autoHeader</span></span>

```xpp
public boolean autoHeader(FieldId field, [boolean orderNo])
```

### <a name="parameters---autoheader"></a><span data-ttu-id="282d4-297">パラメーター - autoHeader</span><span class="sxs-lookup"><span data-stu-id="282d4-297">Parameters - autoHeader</span></span>

<span data-ttu-id="282d4-298"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-298">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-299">orderNo</span><span class="sxs-lookup"><span data-stu-id="282d4-299">orderNo</span></span>  

### <a name="return-value---autoheader"></a><span data-ttu-id="282d4-300">戻り値 - autoHeader</span><span class="sxs-lookup"><span data-stu-id="282d4-300">Return Value - autoHeader</span></span>

## <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="282d4-301">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-301">Method autoHeaderDetailLevel</span></span>

```xpp
public int autoHeaderDetailLevel(FieldId field, [int orderNo])
```

### <a name="parameters---autoheaderdetaillevel"></a><span data-ttu-id="282d4-302">パラメーター - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-302">Parameters - autoHeaderDetailLevel</span></span>

<span data-ttu-id="282d4-303"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-303">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-304">orderNo</span><span class="sxs-lookup"><span data-stu-id="282d4-304">orderNo</span></span>  

### <a name="return-value---autoheaderdetaillevel"></a><span data-ttu-id="282d4-305">戻り値 - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-305">Return Value - autoHeaderDetailLevel</span></span>

## <a name="method-autosum"></a><span data-ttu-id="282d4-306">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="282d4-306">Method autoSum</span></span>

```xpp
public boolean autoSum(FieldId field, [boolean orderNo])
```

### <a name="parameters---autosum"></a><span data-ttu-id="282d4-307">パラメーター - autoSum</span><span class="sxs-lookup"><span data-stu-id="282d4-307">Parameters - autoSum</span></span>

<span data-ttu-id="282d4-308"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-308">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-309">orderNo</span><span class="sxs-lookup"><span data-stu-id="282d4-309">orderNo</span></span>  

### <a name="return-value---autosum"></a><span data-ttu-id="282d4-310">戻り値 - autoSum</span><span class="sxs-lookup"><span data-stu-id="282d4-310">Return Value - autoSum</span></span>

## <a name="method-autosumdetaillevel"></a><span data-ttu-id="282d4-311">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-311">Method autoSumDetailLevel</span></span>

```xpp
public int autoSumDetailLevel(FieldId field, [int orderNo])
```

### <a name="parameters---autosumdetaillevel"></a><span data-ttu-id="282d4-312">パラメーター - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-312">Parameters - autoSumDetailLevel</span></span>

<span data-ttu-id="282d4-313"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-313">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-314">orderNo</span><span class="sxs-lookup"><span data-stu-id="282d4-314">orderNo</span></span>  

### <a name="return-value---autosumdetaillevel"></a><span data-ttu-id="282d4-315">戻り値 - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="282d4-315">Return Value - autoSumDetailLevel</span></span>

## <a name="method-changedno"></a><span data-ttu-id="282d4-316">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="282d4-316">Method changedNo</span></span>

```xpp
public boolean changedNo()
```

### <a name="return-value---changedno"></a><span data-ttu-id="282d4-317">戻り値 - changedNo</span><span class="sxs-lookup"><span data-stu-id="282d4-317">Return Value - changedNo</span></span>

## <a name="method-childdatasourcecount"></a><span data-ttu-id="282d4-318">メソッド childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="282d4-318">Method childDataSourceCount</span></span>

```xpp
public int childDataSourceCount()
```

### <a name="return-value---childdatasourcecount"></a><span data-ttu-id="282d4-319">戻り値 - childDataSourceCount</span><span class="sxs-lookup"><span data-stu-id="282d4-319">Return Value - childDataSourceCount</span></span>

## <a name="method-childdatasourceno"></a><span data-ttu-id="282d4-320">メソッド childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="282d4-320">Method childDataSourceNo</span></span>

```xpp
public QueryBuildDataSource childDataSourceNo(int dataSourceNo)
```

### <a name="parameters---childdatasourceno"></a><span data-ttu-id="282d4-321">パラメーター - childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="282d4-321">Parameters - childDataSourceNo</span></span>

<span data-ttu-id="282d4-322">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="282d4-322">dataSourceNo</span></span>  

### <a name="return-value---childdatasourceno"></a><span data-ttu-id="282d4-323">戻り値 - childDataSourceNo</span><span class="sxs-lookup"><span data-stu-id="282d4-323">Return Value - childDataSourceNo</span></span>

## <a name="method-company"></a><span data-ttu-id="282d4-324">メソッド company</span><span class="sxs-lookup"><span data-stu-id="282d4-324">Method company</span></span>

```xpp
public str company([str value])
```

### <a name="parameters---company"></a><span data-ttu-id="282d4-325">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="282d4-325">Parameters - company</span></span>

<span data-ttu-id="282d4-326">値</span><span class="sxs-lookup"><span data-stu-id="282d4-326">value</span></span>  

### <a name="return-value---company"></a><span data-ttu-id="282d4-327">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="282d4-327">Return Value - company</span></span>

## <a name="method-concurrencymodel"></a><span data-ttu-id="282d4-328">メソッド concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="282d4-328">Method concurrencyModel</span></span>

```xpp
public int concurrencyModel([int value])
```

### <a name="parameters---concurrencymodel"></a><span data-ttu-id="282d4-329">パラメーター - concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="282d4-329">Parameters - concurrencyModel</span></span>

<span data-ttu-id="282d4-330">値</span><span class="sxs-lookup"><span data-stu-id="282d4-330">value</span></span>  

### <a name="return-value---concurrencymodel"></a><span data-ttu-id="282d4-331">戻り値 - concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="282d4-331">Return Value - concurrencyModel</span></span>

## <a name="method-dynalink"></a><span data-ttu-id="282d4-332">メソッド dynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-332">Method dynalink</span></span>

```xpp
public QueryBuildDynalink dynalink(int dynalinkNo)
```

### <a name="parameters---dynalink"></a><span data-ttu-id="282d4-333">パラメーター - dynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-333">Parameters - dynalink</span></span>

<span data-ttu-id="282d4-334">dynalinkNo</span><span class="sxs-lookup"><span data-stu-id="282d4-334">dynalinkNo</span></span>  

### <a name="return-value---dynalink"></a><span data-ttu-id="282d4-335">戻り値 - dynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-335">Return Value - dynalink</span></span>

## <a name="method-dynalinkcount"></a><span data-ttu-id="282d4-336">メソッド dynalinkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-336">Method dynalinkCount</span></span>

```xpp
public int dynalinkCount()
```

### <a name="return-value---dynalinkcount"></a><span data-ttu-id="282d4-337">戻り値 - dynalinkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-337">Return Value - dynalinkCount</span></span>

## <a name="method-embedded"></a><span data-ttu-id="282d4-338">メソッド embedded</span><span class="sxs-lookup"><span data-stu-id="282d4-338">Method embedded</span></span>

```xpp
public boolean embedded()
```

### <a name="return-value---embedded"></a><span data-ttu-id="282d4-339">戻り値 - embedded</span><span class="sxs-lookup"><span data-stu-id="282d4-339">Return Value - embedded</span></span>

## <a name="method-enabled"></a><span data-ttu-id="282d4-340">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="282d4-340">Method enabled</span></span>

<span data-ttu-id="282d4-341">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-341">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="282d4-342">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="282d4-342">Parameters - enabled</span></span>

<span data-ttu-id="282d4-343">値</span><span class="sxs-lookup"><span data-stu-id="282d4-343">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="282d4-344">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="282d4-344">Return Value - enabled</span></span>

<span data-ttu-id="282d4-345">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="282d4-345">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="282d4-346">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="282d4-346">Remarks - enabled</span></span>

<span data-ttu-id="282d4-347">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="282d4-347">The enabled property enables controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="282d4-348">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="282d4-348">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="282d4-349">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="282d4-349">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-existsmeanorexists"></a><span data-ttu-id="282d4-350">メソッド existsMeanOrExists</span><span class="sxs-lookup"><span data-stu-id="282d4-350">Method existsMeanOrExists</span></span>

```xpp
public boolean existsMeanOrExists([boolean value])
```

### <a name="parameters---existsmeanorexists"></a><span data-ttu-id="282d4-351">パラメーター - existsMeanOrExists</span><span class="sxs-lookup"><span data-stu-id="282d4-351">Parameters - existsMeanOrExists</span></span>

<span data-ttu-id="282d4-352">値</span><span class="sxs-lookup"><span data-stu-id="282d4-352">value</span></span>  

### <a name="return-value---existsmeanorexists"></a><span data-ttu-id="282d4-353">戻り値 - existsMeanOrExists</span><span class="sxs-lookup"><span data-stu-id="282d4-353">Return Value - existsMeanOrExists</span></span>

## <a name="method-fetchmode"></a><span data-ttu-id="282d4-354">メソッド fetchMode</span><span class="sxs-lookup"><span data-stu-id="282d4-354">Method fetchMode</span></span>

```xpp
public int fetchMode([int value])
```

### <a name="parameters---fetchmode"></a><span data-ttu-id="282d4-355">パラメーター - fetchMode</span><span class="sxs-lookup"><span data-stu-id="282d4-355">Parameters - fetchMode</span></span>

<span data-ttu-id="282d4-356">値</span><span class="sxs-lookup"><span data-stu-id="282d4-356">value</span></span>  

### <a name="return-value---fetchmode"></a><span data-ttu-id="282d4-357">戻り値 - fetchMode</span><span class="sxs-lookup"><span data-stu-id="282d4-357">Return Value - fetchMode</span></span>

## <a name="method-fields"></a><span data-ttu-id="282d4-358">メソッド fields</span><span class="sxs-lookup"><span data-stu-id="282d4-358">Method fields</span></span>

```xpp
public QueryBuildFieldList fields()
```

### <a name="return-value---fields"></a><span data-ttu-id="282d4-359">戻り値 - fields</span><span class="sxs-lookup"><span data-stu-id="282d4-359">Return Value - fields</span></span>

## <a name="method-file"></a><span data-ttu-id="282d4-360">メソッド file</span><span class="sxs-lookup"><span data-stu-id="282d4-360">Method file</span></span>

```xpp
public TableId file()
```

### <a name="return-value---file"></a><span data-ttu-id="282d4-361">戻り値 - file</span><span class="sxs-lookup"><span data-stu-id="282d4-361">Return Value - file</span></span>

## <a name="method-findrange"></a><span data-ttu-id="282d4-362">メソッド findRange</span><span class="sxs-lookup"><span data-stu-id="282d4-362">Method findRange</span></span>

```xpp
public QueryBuildRange findRange(FieldId field, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findrange"></a><span data-ttu-id="282d4-363">パラメーター - findRange</span><span class="sxs-lookup"><span data-stu-id="282d4-363">Parameters - findRange</span></span>

<span data-ttu-id="282d4-364"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-364">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-365">occurrence</span><span class="sxs-lookup"><span data-stu-id="282d4-365">occurrence</span></span>  

<!-- -->

<span data-ttu-id="282d4-366">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-366">arrayIndex</span></span>  

### <a name="return-value---findrange"></a><span data-ttu-id="282d4-367">戻り値 - findRange</span><span class="sxs-lookup"><span data-stu-id="282d4-367">Return Value - findRange</span></span>

## <a name="method-firstfast"></a><span data-ttu-id="282d4-368">メソッド firstFast</span><span class="sxs-lookup"><span data-stu-id="282d4-368">Method firstFast</span></span>

<span data-ttu-id="282d4-369">他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-369">Determines whether to retrieve the first record from the query before the other records.</span></span>

```xpp
public boolean firstFast([boolean value])
```

### <a name="parameters---firstfast"></a><span data-ttu-id="282d4-370">パラメーター - firstFast</span><span class="sxs-lookup"><span data-stu-id="282d4-370">Parameters - firstFast</span></span>

<span data-ttu-id="282d4-371">値</span><span class="sxs-lookup"><span data-stu-id="282d4-371">value</span></span>  

### <a name="return-value---firstfast"></a><span data-ttu-id="282d4-372">戻り値 - firstFast</span><span class="sxs-lookup"><span data-stu-id="282d4-372">Return Value - firstFast</span></span>

<span data-ttu-id="282d4-373">最初のレコードが最初に取得される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="282d4-373">true if the first record is retrieved first; otherwise, false.</span></span>

### <a name="remarks---firstfast"></a><span data-ttu-id="282d4-374">備考 - firstFast</span><span class="sxs-lookup"><span data-stu-id="282d4-374">Remarks - firstFast</span></span>

<span data-ttu-id="282d4-375">firstFast プロパティは、一部のデータベース システムでレコードの取得を最適化できるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="282d4-375">The firstFast property enables some database systems to optimize record retrieval, which improves performance.</span></span> <span data-ttu-id="282d4-376">データベースはこのプロパティをサポートしていない場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="282d4-376">If the database does not support this property, it is ignored.</span></span>

## <a name="method-firstonly"></a><span data-ttu-id="282d4-377">メソッド firstOnly</span><span class="sxs-lookup"><span data-stu-id="282d4-377">Method firstOnly</span></span>

```xpp
public boolean firstOnly([boolean value])
```

### <a name="parameters---firstonly"></a><span data-ttu-id="282d4-378">パラメーター - firstOnly</span><span class="sxs-lookup"><span data-stu-id="282d4-378">Parameters - firstOnly</span></span>

<span data-ttu-id="282d4-379">値</span><span class="sxs-lookup"><span data-stu-id="282d4-379">value</span></span>  

### <a name="return-value---firstonly"></a><span data-ttu-id="282d4-380">戻り値 - firstOnly</span><span class="sxs-lookup"><span data-stu-id="282d4-380">Return Value - firstOnly</span></span>

## <a name="method-getmostrestrictedquerybuildrangestatus"></a><span data-ttu-id="282d4-381">メソッド getMostRestrictedQueryBuildRangeStatus</span><span class="sxs-lookup"><span data-stu-id="282d4-381">Method getMostRestrictedQueryBuildRangeStatus</span></span>

```xpp
public int getMostRestrictedQueryBuildRangeStatus(FieldId field, [int occurrence], [int arrayIndex])
```

### <a name="parameters---getmostrestrictedquerybuildrangestatus"></a><span data-ttu-id="282d4-382">パラメーター - getMostRestrictedQueryBuildRangeStatus</span><span class="sxs-lookup"><span data-stu-id="282d4-382">Parameters - getMostRestrictedQueryBuildRangeStatus</span></span>

<span data-ttu-id="282d4-383"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-383">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-384">occurrence</span><span class="sxs-lookup"><span data-stu-id="282d4-384">occurrence</span></span>  

<!-- -->

<span data-ttu-id="282d4-385">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-385">arrayIndex</span></span>  

### <a name="return-value---getmostrestrictedquerybuildrangestatus"></a><span data-ttu-id="282d4-386">戻り値 - getMostRestrictedQueryBuildRangeStatus</span><span class="sxs-lookup"><span data-stu-id="282d4-386">Return Value - getMostRestrictedQueryBuildRangeStatus</span></span>

## <a name="method-getno"></a><span data-ttu-id="282d4-387">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="282d4-387">Method getNo</span></span>

```xpp
public Common getNo()
```

### <a name="return-value---getno"></a><span data-ttu-id="282d4-388">戻り値 - getNo</span><span class="sxs-lookup"><span data-stu-id="282d4-388">Return Value - getNo</span></span>

## <a name="method-id"></a><span data-ttu-id="282d4-389">メソッド id</span><span class="sxs-lookup"><span data-stu-id="282d4-389">Method id</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="282d4-390">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="282d4-390">Return Value - id</span></span>

## <a name="method-indexishint"></a><span data-ttu-id="282d4-391">メソッド indexIsHint</span><span class="sxs-lookup"><span data-stu-id="282d4-391">Method indexIsHint</span></span>

```xpp
public boolean indexIsHint(boolean arg)
```

### <a name="parameters---indexishint"></a><span data-ttu-id="282d4-392">パラメーター - indexIsHint</span><span class="sxs-lookup"><span data-stu-id="282d4-392">Parameters - indexIsHint</span></span>

<span data-ttu-id="282d4-393">arg</span><span class="sxs-lookup"><span data-stu-id="282d4-393">arg</span></span>  

### <a name="return-value---indexishint"></a><span data-ttu-id="282d4-394">戻り値 - indexIsHint</span><span class="sxs-lookup"><span data-stu-id="282d4-394">Return Value - indexIsHint</span></span>

## <a name="method-ispartofsubqueryinbasequery"></a><span data-ttu-id="282d4-395">メソッド isPartOfSubQueryInBaseQuery</span><span class="sxs-lookup"><span data-stu-id="282d4-395">Method isPartOfSubQueryInBaseQuery</span></span>

```xpp
public boolean isPartOfSubQueryInBaseQuery()
```

### <a name="return-value---ispartofsubqueryinbasequery"></a><span data-ttu-id="282d4-396">戻り値 - isPartOfSubQueryInBaseQuery</span><span class="sxs-lookup"><span data-stu-id="282d4-396">Return Value - isPartOfSubQueryInBaseQuery</span></span>

## <a name="method-joined"></a><span data-ttu-id="282d4-397">メソッド joined</span><span class="sxs-lookup"><span data-stu-id="282d4-397">Method joined</span></span>

```xpp
public boolean joined()
```

### <a name="return-value---joined"></a><span data-ttu-id="282d4-398">戻り値 - joined</span><span class="sxs-lookup"><span data-stu-id="282d4-398">Return Value - joined</span></span>

## <a name="method-joineddatasources"></a><span data-ttu-id="282d4-399">メソッド joinedDataSources</span><span class="sxs-lookup"><span data-stu-id="282d4-399">Method joinedDataSources</span></span>

```xpp
public container joinedDataSources()
```

### <a name="return-value---joineddatasources"></a><span data-ttu-id="282d4-400">戻り値 - joinedDataSources</span><span class="sxs-lookup"><span data-stu-id="282d4-400">Return Value - joinedDataSources</span></span>

## <a name="method-joinmode"></a><span data-ttu-id="282d4-401">メソッド joinMode</span><span class="sxs-lookup"><span data-stu-id="282d4-401">Method joinMode</span></span>

```xpp
public int joinMode([int value])
```

### <a name="parameters---joinmode"></a><span data-ttu-id="282d4-402">パラメーター - joinMode</span><span class="sxs-lookup"><span data-stu-id="282d4-402">Parameters - joinMode</span></span>

<span data-ttu-id="282d4-403">値</span><span class="sxs-lookup"><span data-stu-id="282d4-403">value</span></span>  

### <a name="return-value---joinmode"></a><span data-ttu-id="282d4-404">戻り値 - joinMode</span><span class="sxs-lookup"><span data-stu-id="282d4-404">Return Value - joinMode</span></span>

## <a name="method-label"></a><span data-ttu-id="282d4-405">メソッド label</span><span class="sxs-lookup"><span data-stu-id="282d4-405">Method label</span></span>

<span data-ttu-id="282d4-406">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-406">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="282d4-407">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="282d4-407">Parameters - label</span></span>

<span data-ttu-id="282d4-408">値</span><span class="sxs-lookup"><span data-stu-id="282d4-408">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="282d4-409">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="282d4-409">Return Value - label</span></span>

<span data-ttu-id="282d4-410">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="282d4-410">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="282d4-411">備考 - label</span><span class="sxs-lookup"><span data-stu-id="282d4-411">Remarks - label</span></span>

<span data-ttu-id="282d4-412">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-412">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="282d4-413">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="282d4-413">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-level"></a><span data-ttu-id="282d4-414">メソッド level</span><span class="sxs-lookup"><span data-stu-id="282d4-414">Method level</span></span>

```xpp
public int level()
```

### <a name="return-value---level"></a><span data-ttu-id="282d4-415">戻り値 - level</span><span class="sxs-lookup"><span data-stu-id="282d4-415">Return Value - level</span></span>

## <a name="method-link"></a><span data-ttu-id="282d4-416">メソッド link</span><span class="sxs-lookup"><span data-stu-id="282d4-416">Method link</span></span>

```xpp
public QueryBuildLink link(int associationNo)
```

### <a name="parameters---link"></a><span data-ttu-id="282d4-417">パラメーター - link</span><span class="sxs-lookup"><span data-stu-id="282d4-417">Parameters - link</span></span>

<span data-ttu-id="282d4-418">associationNo</span><span class="sxs-lookup"><span data-stu-id="282d4-418">associationNo</span></span>  

### <a name="return-value---link"></a><span data-ttu-id="282d4-419">戻り値 - link</span><span class="sxs-lookup"><span data-stu-id="282d4-419">Return Value - link</span></span>

## <a name="method-linkcount"></a><span data-ttu-id="282d4-420">メソッド linkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-420">Method linkCount</span></span>

```xpp
public int linkCount()
```

### <a name="return-value---linkcount"></a><span data-ttu-id="282d4-421">戻り値 - linkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-421">Return Value - linkCount</span></span>

## <a name="method-name"></a><span data-ttu-id="282d4-422">メソッド名</span><span class="sxs-lookup"><span data-stu-id="282d4-422">Method name</span></span>

<span data-ttu-id="282d4-423">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-423">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="282d4-424">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="282d4-424">Parameters - name</span></span>

<span data-ttu-id="282d4-425">値</span><span class="sxs-lookup"><span data-stu-id="282d4-425">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="282d4-426">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="282d4-426">Return Value - name</span></span>

<span data-ttu-id="282d4-427">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="282d4-427">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="282d4-428">備考 - name</span><span class="sxs-lookup"><span data-stu-id="282d4-428">Remarks - name</span></span>

<span data-ttu-id="282d4-429">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="282d4-429">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="282d4-430">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="282d4-430">Begins with a letter.</span></span>
-   <span data-ttu-id="282d4-431">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="282d4-431">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="282d4-432">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="282d4-432">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="282d4-433">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="282d4-433">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="282d4-434">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="282d4-434">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-onetoonedatasources"></a><span data-ttu-id="282d4-435">メソッド oneToOneDataSources</span><span class="sxs-lookup"><span data-stu-id="282d4-435">Method oneToOneDataSources</span></span>

```xpp
public container oneToOneDataSources()
```

### <a name="return-value---onetoonedatasources"></a><span data-ttu-id="282d4-436">戻り値 - oneToOneDataSources</span><span class="sxs-lookup"><span data-stu-id="282d4-436">Return Value - oneToOneDataSources</span></span>

## <a name="method-ordermode"></a><span data-ttu-id="282d4-437">メソッド orderMode</span><span class="sxs-lookup"><span data-stu-id="282d4-437">Method orderMode</span></span>

```xpp
public int orderMode([int value])
```

### <a name="parameters---ordermode"></a><span data-ttu-id="282d4-438">パラメーター - orderMode</span><span class="sxs-lookup"><span data-stu-id="282d4-438">Parameters - orderMode</span></span>

<span data-ttu-id="282d4-439">値</span><span class="sxs-lookup"><span data-stu-id="282d4-439">value</span></span>  

### <a name="return-value---ordermode"></a><span data-ttu-id="282d4-440">戻り値 - orderMode</span><span class="sxs-lookup"><span data-stu-id="282d4-440">Return Value - orderMode</span></span>

## <a name="method-parentdatasource"></a><span data-ttu-id="282d4-441">メソッド parentDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-441">Method parentDataSource</span></span>

```xpp
public QueryBuildDataSource parentDataSource()
```

### <a name="return-value---parentdatasource"></a><span data-ttu-id="282d4-442">戻り値 - parentDataSource</span><span class="sxs-lookup"><span data-stu-id="282d4-442">Return Value - parentDataSource</span></span>

## <a name="method-policycontext"></a><span data-ttu-id="282d4-443">メソッド policyContext</span><span class="sxs-lookup"><span data-stu-id="282d4-443">Method policyContext</span></span>

```xpp
public str policyContext([str value])
```

### <a name="parameters---policycontext"></a><span data-ttu-id="282d4-444">パラメーター - policyContext</span><span class="sxs-lookup"><span data-stu-id="282d4-444">Parameters - policyContext</span></span>

<span data-ttu-id="282d4-445">値</span><span class="sxs-lookup"><span data-stu-id="282d4-445">value</span></span>  

### <a name="return-value---policycontext"></a><span data-ttu-id="282d4-446">戻り値 - policyContext</span><span class="sxs-lookup"><span data-stu-id="282d4-446">Return Value - policyContext</span></span>

## <a name="method-range"></a><span data-ttu-id="282d4-447">メソッド range</span><span class="sxs-lookup"><span data-stu-id="282d4-447">Method range</span></span>

```xpp
public QueryBuildRange range(int rangeNo)
```

### <a name="parameters---range"></a><span data-ttu-id="282d4-448">パラメーター - range</span><span class="sxs-lookup"><span data-stu-id="282d4-448">Parameters - range</span></span>

<span data-ttu-id="282d4-449">rangeNo</span><span class="sxs-lookup"><span data-stu-id="282d4-449">rangeNo</span></span>  

### <a name="return-value---range"></a><span data-ttu-id="282d4-450">戻り値 - range</span><span class="sxs-lookup"><span data-stu-id="282d4-450">Return Value - range</span></span>

## <a name="method-rangecount"></a><span data-ttu-id="282d4-451">メソッド rangeCount</span><span class="sxs-lookup"><span data-stu-id="282d4-451">Method rangeCount</span></span>

```xpp
public int rangeCount()
```

### <a name="return-value---rangecount"></a><span data-ttu-id="282d4-452">戻り値 - rangeCount</span><span class="sxs-lookup"><span data-stu-id="282d4-452">Return Value - rangeCount</span></span>

## <a name="method-rangefield"></a><span data-ttu-id="282d4-453">メソッド rangeField</span><span class="sxs-lookup"><span data-stu-id="282d4-453">Method rangeField</span></span>

```xpp
public QueryBuildRange rangeField(FieldId field, [int occurrence])
```

### <a name="parameters---rangefield"></a><span data-ttu-id="282d4-454">パラメーター - rangeField</span><span class="sxs-lookup"><span data-stu-id="282d4-454">Parameters - rangeField</span></span>

<span data-ttu-id="282d4-455"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-455">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-456">occurrence</span><span class="sxs-lookup"><span data-stu-id="282d4-456">occurrence</span></span>  

### <a name="return-value---rangefield"></a><span data-ttu-id="282d4-457">戻り値 - rangeField</span><span class="sxs-lookup"><span data-stu-id="282d4-457">Return Value - rangeField</span></span>

## <a name="method-relations"></a><span data-ttu-id="282d4-458">メソッド relations</span><span class="sxs-lookup"><span data-stu-id="282d4-458">Method relations</span></span>

```xpp
public boolean relations([boolean value])
```

### <a name="parameters---relations"></a><span data-ttu-id="282d4-459">パラメーター - relations</span><span class="sxs-lookup"><span data-stu-id="282d4-459">Parameters - relations</span></span>

<span data-ttu-id="282d4-460">値</span><span class="sxs-lookup"><span data-stu-id="282d4-460">value</span></span>  

### <a name="return-value---relations"></a><span data-ttu-id="282d4-461">戻り値 - relations</span><span class="sxs-lookup"><span data-stu-id="282d4-461">Return Value - relations</span></span>

## <a name="method-selectioncount"></a><span data-ttu-id="282d4-462">メソッド selectionCount</span><span class="sxs-lookup"><span data-stu-id="282d4-462">Method selectionCount</span></span>

```xpp
public int selectionCount()
```

### <a name="return-value---selectioncount"></a><span data-ttu-id="282d4-463">戻り値 - selectionCount</span><span class="sxs-lookup"><span data-stu-id="282d4-463">Return Value - selectionCount</span></span>

## <a name="method-selectwithrepeatableread"></a><span data-ttu-id="282d4-464">メソッド selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="282d4-464">Method selectWithRepeatableRead</span></span>

```xpp
public boolean selectWithRepeatableRead([boolean value])
```

### <a name="parameters---selectwithrepeatableread"></a><span data-ttu-id="282d4-465">パラメーター - selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="282d4-465">Parameters - selectWithRepeatableRead</span></span>

<span data-ttu-id="282d4-466">値</span><span class="sxs-lookup"><span data-stu-id="282d4-466">value</span></span>  

### <a name="return-value---selectwithrepeatableread"></a><span data-ttu-id="282d4-467">戻り値 - selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="282d4-467">Return Value - selectWithRepeatableRead</span></span>

## <a name="method-sortdirection"></a><span data-ttu-id="282d4-468">メソッド sortDirection</span><span class="sxs-lookup"><span data-stu-id="282d4-468">Method sortDirection</span></span>

```xpp
public SortOrder sortDirection(FieldId field, [SortOrder direction])
```

### <a name="parameters---sortdirection"></a><span data-ttu-id="282d4-469">パラメーター - sortDirection</span><span class="sxs-lookup"><span data-stu-id="282d4-469">Parameters - sortDirection</span></span>

<span data-ttu-id="282d4-470"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-470">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-471">direction</span><span class="sxs-lookup"><span data-stu-id="282d4-471">direction</span></span>  

### <a name="return-value---sortdirection"></a><span data-ttu-id="282d4-472">戻り値 - sortDirection</span><span class="sxs-lookup"><span data-stu-id="282d4-472">Return Value - sortDirection</span></span>

## <a name="method-sortfield"></a><span data-ttu-id="282d4-473">メソッド sortField</span><span class="sxs-lookup"><span data-stu-id="282d4-473">Method sortField</span></span>

```xpp
public FieldId sortField(FieldId field)
```

### <a name="parameters---sortfield"></a><span data-ttu-id="282d4-474">パラメーター - sortField</span><span class="sxs-lookup"><span data-stu-id="282d4-474">Parameters - sortField</span></span>

<span data-ttu-id="282d4-475"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-475">field</span></span>  

### <a name="return-value---sortfield"></a><span data-ttu-id="282d4-476">戻り値 - sortField</span><span class="sxs-lookup"><span data-stu-id="282d4-476">Return Value - sortField</span></span>

## <a name="method-sortfieldcount"></a><span data-ttu-id="282d4-477">メソッド sortFieldCount</span><span class="sxs-lookup"><span data-stu-id="282d4-477">Method sortFieldCount</span></span>

```xpp
public int sortFieldCount()
```

### <a name="return-value---sortfieldcount"></a><span data-ttu-id="282d4-478">戻り値 - sortFieldCount</span><span class="sxs-lookup"><span data-stu-id="282d4-478">Return Value - sortFieldCount</span></span>

## <a name="method-sortindex"></a><span data-ttu-id="282d4-479">メソッド sortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-479">Method sortIndex</span></span>

```xpp
public IndexId sortIndex(int indexNo)
```

### <a name="parameters---sortindex"></a><span data-ttu-id="282d4-480">パラメーター - sortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-480">Parameters - sortIndex</span></span>

<span data-ttu-id="282d4-481">indexNo</span><span class="sxs-lookup"><span data-stu-id="282d4-481">indexNo</span></span>  

### <a name="return-value---sortindex"></a><span data-ttu-id="282d4-482">戻り値 - sortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-482">Return Value - sortIndex</span></span>

## <a name="method-sortindexcount"></a><span data-ttu-id="282d4-483">メソッド sortIndexCount</span><span class="sxs-lookup"><span data-stu-id="282d4-483">Method sortIndexCount</span></span>

```xpp
public int sortIndexCount()
```

### <a name="return-value---sortindexcount"></a><span data-ttu-id="282d4-484">戻り値 - sortIndexCount</span><span class="sxs-lookup"><span data-stu-id="282d4-484">Return Value - sortIndexCount</span></span>

## <a name="method-staticlink"></a><span data-ttu-id="282d4-485">メソッド staticlink</span><span class="sxs-lookup"><span data-stu-id="282d4-485">Method staticlink</span></span>

<span data-ttu-id="282d4-486">クエリのデータ ソースで静的リンク オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-486">Returns a static Link object on the query�s data source.</span></span>

```xpp
public QueryBuildStaticlink staticlink(int staticlinkNo)
```

### <a name="parameters---staticlink"></a><span data-ttu-id="282d4-487">パラメーター - staticlink</span><span class="sxs-lookup"><span data-stu-id="282d4-487">Parameters - staticlink</span></span>

<span data-ttu-id="282d4-488">staticlinkNo</span><span class="sxs-lookup"><span data-stu-id="282d4-488">staticlinkNo</span></span>  

### <a name="return-value---staticlink"></a><span data-ttu-id="282d4-489">戻り値 - staticlink</span><span class="sxs-lookup"><span data-stu-id="282d4-489">Return Value - staticlink</span></span>

<span data-ttu-id="282d4-490">\_staticLinkNo インデックスの静的リンク オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="282d4-490">The static Link object at the \_staticLinkNo index.</span></span>

## <a name="method-staticlinkcount"></a><span data-ttu-id="282d4-491">メソッド staticlinkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-491">Method staticlinkCount</span></span>

<span data-ttu-id="282d4-492">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。</span><span class="sxs-lookup"><span data-stu-id="282d4-492">Gives the number of static links that are defined on the QueryBuildDataSource object.</span></span>

```xpp
public int staticlinkCount()
```

### <a name="return-value---staticlinkcount"></a><span data-ttu-id="282d4-493">戻り値 - staticlinkCount</span><span class="sxs-lookup"><span data-stu-id="282d4-493">Return Value - staticlinkCount</span></span>

<span data-ttu-id="282d4-494">QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数。</span><span class="sxs-lookup"><span data-stu-id="282d4-494">The number of static links that are defined on the QueryBuildDataSource object.</span></span>

## <a name="method-table"></a><span data-ttu-id="282d4-495">メソッド table</span><span class="sxs-lookup"><span data-stu-id="282d4-495">Method table</span></span>

<span data-ttu-id="282d4-496">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-496">Gets or sets the table ID that is associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="282d4-497">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="282d4-497">Parameters - table</span></span>

<span data-ttu-id="282d4-498">値</span><span class="sxs-lookup"><span data-stu-id="282d4-498">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="282d4-499">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="282d4-499">Return Value - table</span></span>

<span data-ttu-id="282d4-500">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="282d4-500">The current value of the table ID that is associated with the object.</span></span>

## <a name="method-tostring"></a><span data-ttu-id="282d4-501">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="282d4-501">Method toString</span></span>

<span data-ttu-id="282d4-502">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-502">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="282d4-503">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="282d4-503">Return Value - toString</span></span>

<span data-ttu-id="282d4-504">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="282d4-504">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="282d4-505">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="282d4-505">Remarks - toString</span></span>

<span data-ttu-id="282d4-506">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-506">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="282d4-507">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="282d4-507">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="282d4-508">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="282d4-508">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-uniontype"></a><span data-ttu-id="282d4-509">メソッド unionType</span><span class="sxs-lookup"><span data-stu-id="282d4-509">Method unionType</span></span>

```xpp
public int unionType([int value])
```

### <a name="parameters---uniontype"></a><span data-ttu-id="282d4-510">パラメーター - unionType</span><span class="sxs-lookup"><span data-stu-id="282d4-510">Parameters - unionType</span></span>

<span data-ttu-id="282d4-511">値</span><span class="sxs-lookup"><span data-stu-id="282d4-511">value</span></span>  

### <a name="return-value---uniontype"></a><span data-ttu-id="282d4-512">戻り値 - unionType</span><span class="sxs-lookup"><span data-stu-id="282d4-512">Return Value - unionType</span></span>

## <a name="method-uniqueid"></a><span data-ttu-id="282d4-513">メソッド uniqueId</span><span class="sxs-lookup"><span data-stu-id="282d4-513">Method uniqueId</span></span>

```xpp
public int uniqueId()
```

### <a name="return-value---uniqueid"></a><span data-ttu-id="282d4-514">戻り値 - uniqueId</span><span class="sxs-lookup"><span data-stu-id="282d4-514">Return Value - uniqueId</span></span>

## <a name="method-update"></a><span data-ttu-id="282d4-515">メソッド update</span><span class="sxs-lookup"><span data-stu-id="282d4-515">Method update</span></span>

<span data-ttu-id="282d4-516">このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="282d4-516">Determines whether the records fetched by this data source can be updated.</span></span>

```xpp
public boolean update([boolean value])
```

### <a name="parameters---update"></a><span data-ttu-id="282d4-517">パラメーター - update</span><span class="sxs-lookup"><span data-stu-id="282d4-517">Parameters - update</span></span>

<span data-ttu-id="282d4-518">値</span><span class="sxs-lookup"><span data-stu-id="282d4-518">value</span></span>  

### <a name="return-value---update"></a><span data-ttu-id="282d4-519">戻り値 - update</span><span class="sxs-lookup"><span data-stu-id="282d4-519">Return Value - update</span></span>

<span data-ttu-id="282d4-520">レコードを更新することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="282d4-520">true if the records can be updated; otherwise, false.</span></span>

### <a name="remarks---update"></a><span data-ttu-id="282d4-521">備考 - update</span><span class="sxs-lookup"><span data-stu-id="282d4-521">Remarks - update</span></span>

<span data-ttu-id="282d4-522">レコードを更新するには、ttsBegin および ttsCommit メソッドを使用して別のトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="282d4-522">To update the records, start a separate transaction by using the ttsBegin and ttsCommit methods.</span></span>

## <a name="method-clearlinks"></a><span data-ttu-id="282d4-523">メソッド clearLinks</span><span class="sxs-lookup"><span data-stu-id="282d4-523">Method clearLinks</span></span>

```xpp
public void clearLinks()
```

## <a name="method-cleardynalinks"></a><span data-ttu-id="282d4-524">メソッド clearDynalinks</span><span class="sxs-lookup"><span data-stu-id="282d4-524">Method clearDynalinks</span></span>

```xpp
public void clearDynalinks()
```

## <a name="method-clearrange"></a><span data-ttu-id="282d4-525">メソッド clearRange</span><span class="sxs-lookup"><span data-stu-id="282d4-525">Method clearRange</span></span>

```xpp
public void clearRange(FieldId field, [int occurrence])
```

### <a name="parameters---clearrange"></a><span data-ttu-id="282d4-526">パラメーター - clearRange</span><span class="sxs-lookup"><span data-stu-id="282d4-526">Parameters - clearRange</span></span>

<span data-ttu-id="282d4-527"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-527">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-528">occurrence</span><span class="sxs-lookup"><span data-stu-id="282d4-528">occurrence</span></span>  

## <a name="method-sortclear"></a><span data-ttu-id="282d4-529">メソッド sortClear</span><span class="sxs-lookup"><span data-stu-id="282d4-529">Method sortClear</span></span>

```xpp
public void sortClear()
```

## <a name="method-finalize"></a><span data-ttu-id="282d4-530">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="282d4-530">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-addselectionfieldwithalias"></a><span data-ttu-id="282d4-531">メソッド addSelectionFieldWithAlias</span><span class="sxs-lookup"><span data-stu-id="282d4-531">Method addSelectionFieldWithAlias</span></span>

```xpp
public void addSelectionFieldWithAlias(str alias, FieldId field, [SelectionField fieldType])
```

### <a name="parameters---addselectionfieldwithalias"></a><span data-ttu-id="282d4-532">パラメーター - addSelectionFieldWithAlias</span><span class="sxs-lookup"><span data-stu-id="282d4-532">Parameters - addSelectionFieldWithAlias</span></span>

<span data-ttu-id="282d4-533">エイリアス</span><span class="sxs-lookup"><span data-stu-id="282d4-533">alias</span></span>  

<!-- -->

<span data-ttu-id="282d4-534"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-534">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-535">fieldType</span><span class="sxs-lookup"><span data-stu-id="282d4-535">fieldType</span></span>  

## <a name="method-addcalculationfield"></a><span data-ttu-id="282d4-536">メソッド addCalculationField</span><span class="sxs-lookup"><span data-stu-id="282d4-536">Method addCalculationField</span></span>

```xpp
public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)
```

### <a name="parameters---addcalculationfield"></a><span data-ttu-id="282d4-537">パラメーター - addCalculationField</span><span class="sxs-lookup"><span data-stu-id="282d4-537">Parameters - addCalculationField</span></span>

<span data-ttu-id="282d4-538">計算</span><span class="sxs-lookup"><span data-stu-id="282d4-538">calculation</span></span>  

<!-- -->

<span data-ttu-id="282d4-539">エイリアス</span><span class="sxs-lookup"><span data-stu-id="282d4-539">alias</span></span>  

## <a name="method-addforeignkeydynalink"></a><span data-ttu-id="282d4-540">メソッド addForeignKeyDynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-540">Method addForeignKeyDynalink</span></span>

```xpp
public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)
```

### <a name="parameters---addforeignkeydynalink"></a><span data-ttu-id="282d4-541">パラメーター - addForeignKeyDynalink</span><span class="sxs-lookup"><span data-stu-id="282d4-541">Parameters - addForeignKeyDynalink</span></span>

<span data-ttu-id="282d4-542">dynamicFile</span><span class="sxs-lookup"><span data-stu-id="282d4-542">dynamicFile</span></span>  

<!-- -->

<span data-ttu-id="282d4-543">relatedRole</span><span class="sxs-lookup"><span data-stu-id="282d4-543">relatedRole</span></span>  

## <a name="method-addrelation"></a><span data-ttu-id="282d4-544">メソッド addRelation</span><span class="sxs-lookup"><span data-stu-id="282d4-544">Method addRelation</span></span>

```xpp
public void addRelation(DictRelation relation, [TableScope tableScope])
```

### <a name="parameters---addrelation"></a><span data-ttu-id="282d4-545">パラメーター - addRelation</span><span class="sxs-lookup"><span data-stu-id="282d4-545">Parameters - addRelation</span></span>

<span data-ttu-id="282d4-546">関係</span><span class="sxs-lookup"><span data-stu-id="282d4-546">relation</span></span>  

<!-- -->

<span data-ttu-id="282d4-547">tableScope</span><span class="sxs-lookup"><span data-stu-id="282d4-547">tableScope</span></span>  

## <a name="method-clearsortindex"></a><span data-ttu-id="282d4-548">メソッド clearSortIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-548">Method clearSortIndex</span></span>

```xpp
public void clearSortIndex()
```

## <a name="method-clearranges"></a><span data-ttu-id="282d4-549">メソッド clearRanges</span><span class="sxs-lookup"><span data-stu-id="282d4-549">Method clearRanges</span></span>

<span data-ttu-id="282d4-550">データ ソースに関連付けられているすべての範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="282d4-550">Deletes all ranges that are associated with the data source.</span></span>

```xpp
public void clearRanges()
```

### <a name="examples---clearranges"></a><span data-ttu-id="282d4-551">例 - clearRanges</span><span class="sxs-lookup"><span data-stu-id="282d4-551">Examples - clearRanges</span></span>

<span data-ttu-id="282d4-552">次の例では、範囲を追加し、データソースから範囲を削除します。</span><span class="sxs-lookup"><span data-stu-id="282d4-552">The following example adds ranges and then removes them from a data source.</span></span>

```xpp
Query Q = new Query(); 
QueryBuildDataSource ds = q.addDataSource(TableNum(CustTable)); 
QueryBuildRange r = ds.addRange(FieldNum(CustTable, recId)); 
print ds.rangeCount(); 
ds.clearRanges(); 
print ds.rangeCount(); 
pause;
```

## <a name="method-linkfields"></a><span data-ttu-id="282d4-553">メソッド linkFields</span><span class="sxs-lookup"><span data-stu-id="282d4-553">Method linkFields</span></span>

```xpp
public void linkFields(str parentField, str thisField, [str parentDatasourceName])
```

### <a name="parameters---linkfields"></a><span data-ttu-id="282d4-554">パラメーター - linkFields</span><span class="sxs-lookup"><span data-stu-id="282d4-554">Parameters - linkFields</span></span>

<span data-ttu-id="282d4-555">parentField</span><span class="sxs-lookup"><span data-stu-id="282d4-555">parentField</span></span>  

<!-- -->

<span data-ttu-id="282d4-556">thisField</span><span class="sxs-lookup"><span data-stu-id="282d4-556">thisField</span></span>  

<!-- -->

<span data-ttu-id="282d4-557">parentDatasourceName</span><span class="sxs-lookup"><span data-stu-id="282d4-557">parentDatasourceName</span></span>  

## <a name="method-addselectionfield"></a><span data-ttu-id="282d4-558">メソッド addSelectionField</span><span class="sxs-lookup"><span data-stu-id="282d4-558">Method addSelectionField</span></span>

```xpp
public void addSelectionField(FieldId field, [SelectionField fieldType], [int arrayIndex])
```

### <a name="parameters---addselectionfield"></a><span data-ttu-id="282d4-559">パラメーター - addSelectionField</span><span class="sxs-lookup"><span data-stu-id="282d4-559">Parameters - addSelectionField</span></span>

<span data-ttu-id="282d4-560"> フィールド</span><span class="sxs-lookup"><span data-stu-id="282d4-560">field</span></span>  

<!-- -->

<span data-ttu-id="282d4-561">fieldType</span><span class="sxs-lookup"><span data-stu-id="282d4-561">fieldType</span></span>  

<!-- -->

<span data-ttu-id="282d4-562">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="282d4-562">arrayIndex</span></span>  

