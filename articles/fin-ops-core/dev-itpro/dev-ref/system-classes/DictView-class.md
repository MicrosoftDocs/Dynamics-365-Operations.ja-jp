---
title: DictView クラス
description: このトピックでは、DictView クラスについて説明します。
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
ms.openlocfilehash: 8d00c99afe8e9e29b94b463af0caebbfee57b1a6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502674"
---
# <a name="class-dictview"></a><span data-ttu-id="223c9-103">クラス DictView</span><span class="sxs-lookup"><span data-stu-id="223c9-103">Class DictView</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictView extends DictTable
```

<span data-ttu-id="223c9-104">DictView クラスでは、特定のビューに関する情報へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="223c9-104">The DictView class provides access to information about a particular view.</span></span>

## <a name="remarks"></a><span data-ttu-id="223c9-105">備考</span><span class="sxs-lookup"><span data-stu-id="223c9-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="223c9-106">例</span><span class="sxs-lookup"><span data-stu-id="223c9-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="223c9-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="223c9-107">Methods</span></span>

| <span data-ttu-id="223c9-108">方法</span><span class="sxs-lookup"><span data-stu-id="223c9-108">Method</span></span>                                                                                                                               | <span data-ttu-id="223c9-109">説明</span><span class="sxs-lookup"><span data-stu-id="223c9-109">Description</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="223c9-110">public str computedColumnString(str dataSourceName, str fieldName, \[FieldNameGenerationMode generationMode\], \[boolean needTrim\])</span><span class="sxs-lookup"><span data-stu-id="223c9-110">public str computedColumnString(str dataSourceName, str fieldName, \[FieldNameGenerationMode generationMode\], \[boolean needTrim\])</span></span> | <span data-ttu-id="223c9-111">テーブル エイリアスを取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-111">Retrieves the table alias.</span></span>                                                                                  |
| <span data-ttu-id="223c9-112">public int datasourceCnt()</span><span class="sxs-lookup"><span data-stu-id="223c9-112">public int datasourceCnt()</span></span>                                                                                                           | <span data-ttu-id="223c9-113">ビュー内のデータ ソースをカウントします。</span><span class="sxs-lookup"><span data-stu-id="223c9-113">Counts data sources in the view.</span></span>                                                                            |
| <span data-ttu-id="223c9-114">public str datasourceDataareaIdName(int cnt)</span><span class="sxs-lookup"><span data-stu-id="223c9-114">public str datasourceDataareaIdName(int cnt)</span></span>                                                                                         | <span data-ttu-id="223c9-115">データ ソースの法人を識別するためにビュー定義で使用される SQL 名を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-115">Retrieves the SQL name that is used in the view definition to identify the legal entity of the data source.</span></span> |
| <span data-ttu-id="223c9-116">public TableId datasourceID2TableId(TableId dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="223c9-116">public TableId datasourceID2TableId(TableId dataSourceId)</span></span>                                                                            | <span data-ttu-id="223c9-117">特定のデータ ソースのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-117">Gets the table ID of the given data source.</span></span>                                                                 |
| <span data-ttu-id="223c9-118">public TableId datasourceTableId(int cnt)</span><span class="sxs-lookup"><span data-stu-id="223c9-118">public TableId datasourceTableId(int cnt)</span></span>                                                                                            | <span data-ttu-id="223c9-119">インデックス化されたデータ ソースのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-119">Retrieves the table ID of the indexed data source.</span></span>                                                          |
| <span data-ttu-id="223c9-120">public SelectionField fieldAggregation(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="223c9-120">public SelectionField fieldAggregation(FieldId fieldId)</span></span>                                                                              | <span data-ttu-id="223c9-121">特定のフィールドが実行する集計の種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-121">Retrieves the type of aggregation that a given field performs.</span></span>                                              |
| <span data-ttu-id="223c9-122">public int fieldDatasource(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="223c9-122">public int fieldDatasource(FieldId fieldId)</span></span>                                                                                          | <span data-ttu-id="223c9-123">特定のフィールドの発生元データ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-123">Retrieves the ID of the data source that the given field originates from.</span></span>                                   |
| <span data-ttu-id="223c9-124">public TableId fieldDatasourceID(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="223c9-124">public TableId fieldDatasourceID(FieldId fieldId)</span></span>                                                                                    | <span data-ttu-id="223c9-125">特定のフィールドがマッピングされるビューでデータ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-125">Retrieves the ID of the data source in the view that the given field maps to.</span></span>                               |
| <span data-ttu-id="223c9-126">public FieldId fieldId(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="223c9-126">public FieldId fieldId(FieldId fieldId)</span></span>                                                                                              | <span data-ttu-id="223c9-127">元のテーブルのフィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-127">Retrieves the field ID from the underlying table.</span></span>                                                           |
| <span data-ttu-id="223c9-128">public boolean isAggregatedView()</span><span class="sxs-lookup"><span data-stu-id="223c9-128">public boolean isAggregatedView()</span></span>                                                                                                    | <span data-ttu-id="223c9-129">ビューが集約されているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="223c9-129">Checks whether the view is aggregated.</span></span>                                                                      |
| <span data-ttu-id="223c9-130">public Query query()</span><span class="sxs-lookup"><span data-stu-id="223c9-130">public Query query()</span></span>                                                                                                                 |                                                                                                             |
| <span data-ttu-id="223c9-131">public boolean isDataEntity()</span><span class="sxs-lookup"><span data-stu-id="223c9-131">public boolean isDataEntity()</span></span>                                                                                                        |                                                                                                             |
| <span data-ttu-id="223c9-132">public boolean isUpdatable()</span><span class="sxs-lookup"><span data-stu-id="223c9-132">public boolean isUpdatable()</span></span>                                                                                                         |                                                                                                             |
| <span data-ttu-id="223c9-133">public boolean isPublic()</span><span class="sxs-lookup"><span data-stu-id="223c9-133">public boolean isPublic()</span></span>                                                                                                            |                                                                                                             |
| <span data-ttu-id="223c9-134">public str collectionName()</span><span class="sxs-lookup"><span data-stu-id="223c9-134">public str collectionName()</span></span>                                                                                                          |                                                                                                             |
| <span data-ttu-id="223c9-135">public boolean isVirtualField(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="223c9-135">public boolean isVirtualField(str fieldName)</span></span>                                                                                         |                                                                                                             |
| <span data-ttu-id="223c9-136">public FieldAccessModifier getFieldAccessModifier(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="223c9-136">public FieldAccessModifier getFieldAccessModifier(str fieldName)</span></span>                                                                     |                                                                                                             |
| <span data-ttu-id="223c9-137">public boolean isStaged()</span><span class="sxs-lookup"><span data-stu-id="223c9-137">public boolean isStaged()</span></span>                                                                                                            |                                                                                                             |
| <span data-ttu-id="223c9-138">public str version()</span><span class="sxs-lookup"><span data-stu-id="223c9-138">public str version()</span></span>                                                                                                                 |                                                                                                             |
| <span data-ttu-id="223c9-139">public MessagingRole messagingRole()</span><span class="sxs-lookup"><span data-stu-id="223c9-139">public MessagingRole messagingRole()</span></span>                                                                                                 |                                                                                                             |
| <span data-ttu-id="223c9-140">public void new(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="223c9-140">public void new(TableId tableId)</span></span>                                                                                                     | <span data-ttu-id="223c9-141">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="223c9-141">Initializes a new instance of the Object class.</span></span>                                                             |

## <a name="method-computedcolumnstring"></a><span data-ttu-id="223c9-142">メソッド computedColumnString</span><span class="sxs-lookup"><span data-stu-id="223c9-142">Method computedColumnString</span></span>

<span data-ttu-id="223c9-143">テーブル エイリアスを取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-143">Retrieves the table alias.</span></span>

```xpp
public str computedColumnString(str dataSourceName, str fieldName, [FieldNameGenerationMode generationMode], [boolean needTrim])
```

### <a name="parameters---computedcolumnstring"></a><span data-ttu-id="223c9-144">パラメーター - computedColumnString</span><span class="sxs-lookup"><span data-stu-id="223c9-144">Parameters - computedColumnString</span></span>

<span data-ttu-id="223c9-145">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="223c9-145">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="223c9-146">fieldName</span><span class="sxs-lookup"><span data-stu-id="223c9-146">fieldName</span></span>  

<!-- -->

<span data-ttu-id="223c9-147">generationMode</span><span class="sxs-lookup"><span data-stu-id="223c9-147">generationMode</span></span>  

<!-- -->

<span data-ttu-id="223c9-148">needTrim</span><span class="sxs-lookup"><span data-stu-id="223c9-148">needTrim</span></span>  

### <a name="return-value---computedcolumnstring"></a><span data-ttu-id="223c9-149">戻り値 - computedColumnString</span><span class="sxs-lookup"><span data-stu-id="223c9-149">Return Value - computedColumnString</span></span>

<span data-ttu-id="223c9-150">書式設定されたフィールド名文字列。</span><span class="sxs-lookup"><span data-stu-id="223c9-150">The formatted field name string.</span></span>

### <a name="remarks---computedcolumnstring"></a><span data-ttu-id="223c9-151">備考 - computedColumnString</span><span class="sxs-lookup"><span data-stu-id="223c9-151">Remarks - computedColumnString</span></span>

<span data-ttu-id="223c9-152">テーブルのエイリアスは、計算列定義と一緒に使用できるデータベース形式の SQL フィールド名です。</span><span class="sxs-lookup"><span data-stu-id="223c9-152">The table alias is an SQL field name in a database-style format that can be used together with a computed column definition.</span></span>

## <a name="method-datasourcecnt"></a><span data-ttu-id="223c9-153">メソッド datasourceCnt</span><span class="sxs-lookup"><span data-stu-id="223c9-153">Method datasourceCnt</span></span>

<span data-ttu-id="223c9-154">ビュー内のデータ ソースをカウントします。</span><span class="sxs-lookup"><span data-stu-id="223c9-154">Counts data sources in the view.</span></span>

```xpp
public int datasourceCnt()
```

### <a name="return-value---datasourcecnt"></a><span data-ttu-id="223c9-155">戻り値 - datasourceCnt</span><span class="sxs-lookup"><span data-stu-id="223c9-155">Return Value - datasourceCnt</span></span>

<span data-ttu-id="223c9-156">ビュー内のデータ ソースの数。</span><span class="sxs-lookup"><span data-stu-id="223c9-156">The number of data sources in the view.</span></span>

## <a name="method-datasourcedataareaidname"></a><span data-ttu-id="223c9-157">メソッド datasourceDataareaIdName</span><span class="sxs-lookup"><span data-stu-id="223c9-157">Method datasourceDataareaIdName</span></span>

<span data-ttu-id="223c9-158">データ ソースの法人を識別するためにビュー定義で使用される SQL 名を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-158">Retrieves the SQL name that is used in the view definition to identify the legal entity of the data source.</span></span>

```xpp
public str datasourceDataareaIdName(int cnt)
```

### <a name="parameters---datasourcedataareaidname"></a><span data-ttu-id="223c9-159">パラメーター - datasourceDataareaIdName</span><span class="sxs-lookup"><span data-stu-id="223c9-159">Parameters - datasourceDataareaIdName</span></span>

<span data-ttu-id="223c9-160">cnt</span><span class="sxs-lookup"><span data-stu-id="223c9-160">cnt</span></span>  

### <a name="return-value---datasourcedataareaidname"></a><span data-ttu-id="223c9-161">戻り値 - datasourceDataareaIdName</span><span class="sxs-lookup"><span data-stu-id="223c9-161">Return Value - datasourceDataareaIdName</span></span>

<span data-ttu-id="223c9-162">データ ソースの法人を識別するためにビュー定義で使用される SQL 名。エラーが発生した場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="223c9-162">The SQL name that is used in the view definition to identify the legal entity of the data source; an empty string if an error occurs.</span></span>

## <a name="method-datasourceid2tableid"></a><span data-ttu-id="223c9-163">メソッド datasourceID2TableId</span><span class="sxs-lookup"><span data-stu-id="223c9-163">Method datasourceID2TableId</span></span>

<span data-ttu-id="223c9-164">特定のデータ ソースのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-164">Gets the table ID of the given data source.</span></span>

```xpp
public TableId datasourceID2TableId(TableId dataSourceId)
```

### <a name="parameters---datasourceid2tableid"></a><span data-ttu-id="223c9-165">パラメーター - datasourceID2TableId</span><span class="sxs-lookup"><span data-stu-id="223c9-165">Parameters - datasourceID2TableId</span></span>

<span data-ttu-id="223c9-166">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="223c9-166">dataSourceId</span></span>  

### <a name="return-value---datasourceid2tableid"></a><span data-ttu-id="223c9-167">戻り値 - datasourceID2TableId</span><span class="sxs-lookup"><span data-stu-id="223c9-167">Return Value - datasourceID2TableId</span></span>

<span data-ttu-id="223c9-168">特定のデータ ソースのテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="223c9-168">The table ID of the given data source.</span></span>

## <a name="method-datasourcetableid"></a><span data-ttu-id="223c9-169">メソッド datasourceTableId</span><span class="sxs-lookup"><span data-stu-id="223c9-169">Method datasourceTableId</span></span>

<span data-ttu-id="223c9-170">インデックス化されたデータ ソースのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-170">Retrieves the table ID of the indexed data source.</span></span>

```xpp
public TableId datasourceTableId(int cnt)
```

### <a name="parameters---datasourcetableid"></a><span data-ttu-id="223c9-171">パラメーター - datasourceTableId</span><span class="sxs-lookup"><span data-stu-id="223c9-171">Parameters - datasourceTableId</span></span>

<span data-ttu-id="223c9-172">cnt</span><span class="sxs-lookup"><span data-stu-id="223c9-172">cnt</span></span>  

### <a name="return-value---datasourcetableid"></a><span data-ttu-id="223c9-173">戻り値 - datasourceTableId</span><span class="sxs-lookup"><span data-stu-id="223c9-173">Return Value - datasourceTableId</span></span>

<span data-ttu-id="223c9-174">指定されたデータ ソースのテーブル ID。エラーが発生した場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="223c9-174">The table ID of the given data source; 0 (zero) if an error occurs.</span></span>

## <a name="method-fieldaggregation"></a><span data-ttu-id="223c9-175">メソッド fieldAggregation</span><span class="sxs-lookup"><span data-stu-id="223c9-175">Method fieldAggregation</span></span>

<span data-ttu-id="223c9-176">特定のフィールドが実行する集計の種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-176">Retrieves the type of aggregation that a given field performs.</span></span>

```xpp
public SelectionField fieldAggregation(FieldId fieldId)
```

### <a name="parameters---fieldaggregation"></a><span data-ttu-id="223c9-177">パラメーター - fieldAggregation</span><span class="sxs-lookup"><span data-stu-id="223c9-177">Parameters - fieldAggregation</span></span>

<span data-ttu-id="223c9-178">fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-178">fieldId</span></span>  

### <a name="return-value---fieldaggregation"></a><span data-ttu-id="223c9-179">戻り値 - fieldAggregation</span><span class="sxs-lookup"><span data-stu-id="223c9-179">Return Value - fieldAggregation</span></span>

<span data-ttu-id="223c9-180">集約のタイプ。</span><span class="sxs-lookup"><span data-stu-id="223c9-180">The type of aggregation.</span></span>

## <a name="method-fielddatasource"></a><span data-ttu-id="223c9-181">メソッド fieldDatasource</span><span class="sxs-lookup"><span data-stu-id="223c9-181">Method fieldDatasource</span></span>

<span data-ttu-id="223c9-182">特定のフィールドの発生元データ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-182">Retrieves the ID of the data source that the given field originates from.</span></span>

```xpp
public int fieldDatasource(FieldId fieldId)
```

### <a name="parameters---fielddatasource"></a><span data-ttu-id="223c9-183">パラメーター - fieldDatasource</span><span class="sxs-lookup"><span data-stu-id="223c9-183">Parameters - fieldDatasource</span></span>

<span data-ttu-id="223c9-184">fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-184">fieldId</span></span>  

### <a name="return-value---fielddatasource"></a><span data-ttu-id="223c9-185">戻り値 - fieldDatasource</span><span class="sxs-lookup"><span data-stu-id="223c9-185">Return Value - fieldDatasource</span></span>

<span data-ttu-id="223c9-186">データ ソース ID。</span><span class="sxs-lookup"><span data-stu-id="223c9-186">The data source ID.</span></span>

## <a name="method-fielddatasourceid"></a><span data-ttu-id="223c9-187">メソッド fieldDatasourceID</span><span class="sxs-lookup"><span data-stu-id="223c9-187">Method fieldDatasourceID</span></span>

<span data-ttu-id="223c9-188">特定のフィールドがマッピングされるビューでデータ ソースの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-188">Retrieves the ID of the data source in the view that the given field maps to.</span></span>

```xpp
public TableId fieldDatasourceID(FieldId fieldId)
```

### <a name="parameters---fielddatasourceid"></a><span data-ttu-id="223c9-189">パラメーター - fieldDatasourceID</span><span class="sxs-lookup"><span data-stu-id="223c9-189">Parameters - fieldDatasourceID</span></span>

<span data-ttu-id="223c9-190">fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-190">fieldId</span></span>  

### <a name="return-value---fielddatasourceid"></a><span data-ttu-id="223c9-191">戻り値 - fieldDatasourceID</span><span class="sxs-lookup"><span data-stu-id="223c9-191">Return Value - fieldDatasourceID</span></span>

<span data-ttu-id="223c9-192">データ ソース ID。</span><span class="sxs-lookup"><span data-stu-id="223c9-192">The data source ID.</span></span>

## <a name="method-fieldid"></a><span data-ttu-id="223c9-193">メソッド fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-193">Method fieldId</span></span>

<span data-ttu-id="223c9-194">元のテーブルのフィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="223c9-194">Retrieves the field ID from the underlying table.</span></span>

```xpp
public FieldId fieldId(FieldId fieldId)
```

### <a name="parameters---fieldid"></a><span data-ttu-id="223c9-195">パラメーター - fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-195">Parameters - fieldId</span></span>

<span data-ttu-id="223c9-196">fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-196">fieldId</span></span>  

### <a name="return-value---fieldid"></a><span data-ttu-id="223c9-197">戻り値 - fieldId</span><span class="sxs-lookup"><span data-stu-id="223c9-197">Return Value - fieldId</span></span>

<span data-ttu-id="223c9-198">基になるテーブルのフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="223c9-198">The field ID from the underlying table.</span></span>

## <a name="method-isaggregatedview"></a><span data-ttu-id="223c9-199">メソッド isAggregatedView</span><span class="sxs-lookup"><span data-stu-id="223c9-199">Method isAggregatedView</span></span>

<span data-ttu-id="223c9-200">ビューが集約されているかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="223c9-200">Checks whether the view is aggregated.</span></span>

```xpp
public boolean isAggregatedView()
```

### <a name="return-value---isaggregatedview"></a><span data-ttu-id="223c9-201">戻り値 - isAggregatedView</span><span class="sxs-lookup"><span data-stu-id="223c9-201">Return Value - isAggregatedView</span></span>

<span data-ttu-id="223c9-202">ビューが集計される場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="223c9-202">true if the view is aggregated; otherwise, false.</span></span>

## <a name="method-query"></a><span data-ttu-id="223c9-203">メソッド query</span><span class="sxs-lookup"><span data-stu-id="223c9-203">Method query</span></span>

```xpp
public Query query()
```

### <a name="return-value---query"></a><span data-ttu-id="223c9-204">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="223c9-204">Return Value - query</span></span>

## <a name="method-isdataentity"></a><span data-ttu-id="223c9-205">メソッド isDataEntity</span><span class="sxs-lookup"><span data-stu-id="223c9-205">Method isDataEntity</span></span>

```xpp
public boolean isDataEntity()
```

### <a name="return-value---isdataentity"></a><span data-ttu-id="223c9-206">戻り値 - isDataEntity</span><span class="sxs-lookup"><span data-stu-id="223c9-206">Return Value - isDataEntity</span></span>

## <a name="method-isupdatable"></a><span data-ttu-id="223c9-207">メソッド isUpdatable</span><span class="sxs-lookup"><span data-stu-id="223c9-207">Method isUpdatable</span></span>

```xpp
public boolean isUpdatable()
```

### <a name="return-value---isupdatable"></a><span data-ttu-id="223c9-208">戻り値 - isUpdatable</span><span class="sxs-lookup"><span data-stu-id="223c9-208">Return Value - isUpdatable</span></span>

## <a name="method-ispublic"></a><span data-ttu-id="223c9-209">メソッド isPublic</span><span class="sxs-lookup"><span data-stu-id="223c9-209">Method isPublic</span></span>

```xpp
public boolean isPublic()
```

### <a name="return-value---ispublic"></a><span data-ttu-id="223c9-210">戻り値 - isPublic</span><span class="sxs-lookup"><span data-stu-id="223c9-210">Return Value - isPublic</span></span>

## <a name="method-collectionname"></a><span data-ttu-id="223c9-211">メソッド collectionName</span><span class="sxs-lookup"><span data-stu-id="223c9-211">Method collectionName</span></span>

```xpp
public str collectionName()
```

### <a name="return-value---collectionname"></a><span data-ttu-id="223c9-212">戻り値 - collectionName</span><span class="sxs-lookup"><span data-stu-id="223c9-212">Return Value - collectionName</span></span>

## <a name="method-isvirtualfield"></a><span data-ttu-id="223c9-213">メソッド isVirtualField</span><span class="sxs-lookup"><span data-stu-id="223c9-213">Method isVirtualField</span></span>

```xpp
public boolean isVirtualField(str fieldName)
```

### <a name="parameters---isvirtualfield"></a><span data-ttu-id="223c9-214">パラメーター - isVirtualField</span><span class="sxs-lookup"><span data-stu-id="223c9-214">Parameters - isVirtualField</span></span>

<span data-ttu-id="223c9-215">fieldName</span><span class="sxs-lookup"><span data-stu-id="223c9-215">fieldName</span></span>  

### <a name="return-value---isvirtualfield"></a><span data-ttu-id="223c9-216">戻り値 - isVirtualField</span><span class="sxs-lookup"><span data-stu-id="223c9-216">Return Value - isVirtualField</span></span>

## <a name="method-getfieldaccessmodifier"></a><span data-ttu-id="223c9-217">メソッド getFieldAccessModifier</span><span class="sxs-lookup"><span data-stu-id="223c9-217">Method getFieldAccessModifier</span></span>

```xpp
public FieldAccessModifier getFieldAccessModifier(str fieldName)
```

### <a name="parameters---getfieldaccessmodifier"></a><span data-ttu-id="223c9-218">パラメーター - getFieldAccessModifier</span><span class="sxs-lookup"><span data-stu-id="223c9-218">Parameters - getFieldAccessModifier</span></span>

<span data-ttu-id="223c9-219">fieldName</span><span class="sxs-lookup"><span data-stu-id="223c9-219">fieldName</span></span>  

### <a name="return-value---getfieldaccessmodifier"></a><span data-ttu-id="223c9-220">戻り値 - getFieldAccessModifier</span><span class="sxs-lookup"><span data-stu-id="223c9-220">Return Value - getFieldAccessModifier</span></span>

## <a name="method-isstaged"></a><span data-ttu-id="223c9-221">メソッド isStaged</span><span class="sxs-lookup"><span data-stu-id="223c9-221">Method isStaged</span></span>

```xpp
public boolean isStaged()
```

### <a name="return-value---isstaged"></a><span data-ttu-id="223c9-222">戻り値 - isStaged</span><span class="sxs-lookup"><span data-stu-id="223c9-222">Return Value - isStaged</span></span>

## <a name="method-version"></a><span data-ttu-id="223c9-223">メソッド version</span><span class="sxs-lookup"><span data-stu-id="223c9-223">Method version</span></span>

```xpp
public str version()
```

### <a name="return-value---version"></a><span data-ttu-id="223c9-224">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="223c9-224">Return Value - version</span></span>

## <a name="method-messagingrole"></a><span data-ttu-id="223c9-225">メソッド messagingRole</span><span class="sxs-lookup"><span data-stu-id="223c9-225">Method messagingRole</span></span>

```xpp
public MessagingRole messagingRole()
```

### <a name="return-value---messagingrole"></a><span data-ttu-id="223c9-226">戻り値 - messagingRole</span><span class="sxs-lookup"><span data-stu-id="223c9-226">Return Value - messagingRole</span></span>

## <a name="method-new"></a><span data-ttu-id="223c9-227">メソッド new</span><span class="sxs-lookup"><span data-stu-id="223c9-227">Method new</span></span>

<span data-ttu-id="223c9-228">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="223c9-228">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a><span data-ttu-id="223c9-229">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="223c9-229">Parameters - new</span></span>

<span data-ttu-id="223c9-230">tableId</span><span class="sxs-lookup"><span data-stu-id="223c9-230">tableId</span></span>  
<span data-ttu-id="223c9-231">クラス インスタンスの作成に使用するテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="223c9-231">The table ID to use to create the class instance.</span></span>

