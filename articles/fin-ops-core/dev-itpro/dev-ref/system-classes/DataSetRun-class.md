---
title: DataSetRun クラス
description: このトピックでは、DataSetRun クラスについて説明します。
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
ms.openlocfilehash: d28bb8fb5b3264abfc9a7e37fc6c718d7d291de3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502735"
---
# <a name="class-datasetrun"></a><span data-ttu-id="e03d1-103">クラス DataSetRun</span><span class="sxs-lookup"><span data-stu-id="e03d1-103">Class DataSetRun</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataSetRun extends ObjectRun
```

## <a name="remarks"></a><span data-ttu-id="e03d1-104">備考</span><span class="sxs-lookup"><span data-stu-id="e03d1-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e03d1-105">例</span><span class="sxs-lookup"><span data-stu-id="e03d1-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e03d1-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e03d1-106">Methods</span></span>

| <span data-ttu-id="e03d1-107">方法</span><span class="sxs-lookup"><span data-stu-id="e03d1-107">Method</span></span>                                                                                                                                                                              | <span data-ttu-id="e03d1-108">説明</span><span class="sxs-lookup"><span data-stu-id="e03d1-108">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="e03d1-109">public FormDataSource addDataSource(TableId tableId, \[str joinDataSourceName\], \[DataSourceLinkTypePropertyValues linkType\], \[FieldId joinFieldId\], \[str newDataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-109">public FormDataSource addDataSource(TableId tableId, \[str joinDataSourceName\], \[DataSourceLinkTypePropertyValues linkType\], \[FieldId joinFieldId\], \[str newDataSourceName\])</span></span> | <span data-ttu-id="e03d1-110">dataSetRun クラスに新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-110">Adds a new data source to the dataSetRun class.</span></span>                               |
| <span data-ttu-id="e03d1-111">public DataSet dataSet()</span><span class="sxs-lookup"><span data-stu-id="e03d1-111">public DataSet dataSet()</span></span>                                                                                                                                                            |                                                                               |
| <span data-ttu-id="e03d1-112">public FormObjectSet dataSource(\[AnyType objectSet\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-112">public FormObjectSet dataSource(\[AnyType objectSet\])</span></span>                                                                                                                              |                                                                               |
| <span data-ttu-id="e03d1-113">public FormObjectSet dataSourceById(int id)</span><span class="sxs-lookup"><span data-stu-id="e03d1-113">public FormObjectSet dataSourceById(int id)</span></span>                                                                                                                                         |                                                                               |
| <span data-ttu-id="e03d1-114">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="e03d1-114">public int dataSourceCount()</span></span>                                                                                                                                                        |                                                                               |
| <span data-ttu-id="e03d1-115">public Array getActiveFields(int dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="e03d1-115">public Array getActiveFields(int dataSourceId)</span></span>                                                                                                                                      |                                                                               |
| <span data-ttu-id="e03d1-116">public container getChildrenById(str dataSourceName, \[AnyType parentId\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-116">public container getChildrenById(str dataSourceName, \[AnyType parentId\])</span></span>                                                                                                          | <span data-ttu-id="e03d1-117">親 ID を使用してデータ ソースの子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-117">Gets the children of a data source by using the parent ID.</span></span>                    |
| <span data-ttu-id="e03d1-118">public container getChildrenByIndex(str dataSourceName, \[int parentIndex\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-118">public container getChildrenByIndex(str dataSourceName, \[int parentIndex\])</span></span>                                                                                                        | <span data-ttu-id="e03d1-119">親インデックスを使用してデータ ソースの子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-119">Gets the children of a data source by using the parent index.</span></span>                 |
| <span data-ttu-id="e03d1-120">public DataSetError getLastError()</span><span class="sxs-lookup"><span data-stu-id="e03d1-120">public DataSetError getLastError()</span></span>                                                                                                                                                  |                                                                               |
| <span data-ttu-id="e03d1-121">public AnyType getParentById(str dataSourceName, AnyType childId)</span><span class="sxs-lookup"><span data-stu-id="e03d1-121">public AnyType getParentById(str dataSourceName, AnyType childId)</span></span>                                                                                                                   | <span data-ttu-id="e03d1-122">子 ID を使用してデータ ソースの親を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-122">Gets the parent of a data source by using the child ID.</span></span>                       |
| <span data-ttu-id="e03d1-123">public int getParentByIndex(str dataSourceName, int childIndex)</span><span class="sxs-lookup"><span data-stu-id="e03d1-123">public int getParentByIndex(str dataSourceName, int childIndex)</span></span>                                                                                                                     | <span data-ttu-id="e03d1-124">子インデックスを使用してデータ ソースの親を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-124">Gets the parent of a data source by using the child index.</span></span>                    |
| <span data-ttu-id="e03d1-125">public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)</span><span class="sxs-lookup"><span data-stu-id="e03d1-125">public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)</span></span>                                                                                                            | <span data-ttu-id="e03d1-126">行階層 ID を使用してデータ ソース内の行インデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-126">Gets the row index on a data source by using a row hierarchy ID.</span></span>              |
| <span data-ttu-id="e03d1-127">public boolean initComplete()</span><span class="sxs-lookup"><span data-stu-id="e03d1-127">public boolean initComplete()</span></span>                                                                                                                                                       |                                                                               |
| <span data-ttu-id="e03d1-128">public str name()</span><span class="sxs-lookup"><span data-stu-id="e03d1-128">public str name()</span></span>                                                                                                                                                                   |                                                                               |
| <span data-ttu-id="e03d1-129">public FormObjectSet objectSet(\[AnyType objectSet\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-129">public FormObjectSet objectSet(\[AnyType objectSet\])</span></span>                                                                                                                               |                                                                               |
| <span data-ttu-id="e03d1-130">public container pack()</span><span class="sxs-lookup"><span data-stu-id="e03d1-130">public container pack()</span></span>                                                                                                                                                             | <span data-ttu-id="e03d1-131">DataSetRun クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-131">Serializes the current instance of the DataSetRun class.</span></span>                      |
| <span data-ttu-id="e03d1-132">public boolean runCalled()</span><span class="sxs-lookup"><span data-stu-id="e03d1-132">public boolean runCalled()</span></span>                                                                                                                                                          |                                                                               |
| <span data-ttu-id="e03d1-133">public boolean unpack(container pack)</span><span class="sxs-lookup"><span data-stu-id="e03d1-133">public boolean unpack(container pack)</span></span>                                                                                                                                               | <span data-ttu-id="e03d1-134">pack パラメーター値を DataSetRun クラスのインスタンスに逆シリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-134">Deserializes the pack parameter value to an instance of the DataSetRun class.</span></span> |
| <span data-ttu-id="e03d1-135">::public static DataSetRun create(str name, container pack)</span><span class="sxs-lookup"><span data-stu-id="e03d1-135">::public static DataSetRun create(str name, container pack)</span></span>                                                                                                                         |                                                                               |
| <span data-ttu-id="e03d1-136">::public static DataSetRun createRunTime(container pack)</span><span class="sxs-lookup"><span data-stu-id="e03d1-136">::public static DataSetRun createRunTime(container pack)</span></span>                                                                                                                            |                                                                               |
| <span data-ttu-id="e03d1-137">public void setLastError(DataSetError error)</span><span class="sxs-lookup"><span data-stu-id="e03d1-137">public void setLastError(DataSetError error)</span></span>                                                                                                                                        |                                                                               |
| <span data-ttu-id="e03d1-138">public void run()</span><span class="sxs-lookup"><span data-stu-id="e03d1-138">public void run()</span></span>                                                                                                                                                                   |                                                                               |
| <span data-ttu-id="e03d1-139">public void setLookupMode()</span><span class="sxs-lookup"><span data-stu-id="e03d1-139">public void setLookupMode()</span></span>                                                                                                                                                         | <span data-ttu-id="e03d1-140">データセットをルックアップ モードにします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-140">Puts the dataset into lookup mode.</span></span>                                            |
| <span data-ttu-id="e03d1-141">public void new(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="e03d1-141">public void new(xArgs args)</span></span>                                                                                                                                                         | <span data-ttu-id="e03d1-142">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-142">Initializes a new instance of the Object class.</span></span>                               |
| <span data-ttu-id="e03d1-143">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="e03d1-143">public void finalize()</span></span>                                                                                                                                                              |                                                                               |
| <span data-ttu-id="e03d1-144">public void createRecord(str formDataSourceName, \[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-144">public void createRecord(str formDataSourceName, \[boolean append\])</span></span>                                                                                                                | <span data-ttu-id="e03d1-145">新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-145">Creates a new record.</span></span>                                                         |
| <span data-ttu-id="e03d1-146">public void setActiveFields(int dataSourceId, Array fieldIds)</span><span class="sxs-lookup"><span data-stu-id="e03d1-146">public void setActiveFields(int dataSourceId, Array fieldIds)</span></span>                                                                                                                       |                                                                               |
| <span data-ttu-id="e03d1-147">public void setExternalContext(\[Common externalContext\])</span><span class="sxs-lookup"><span data-stu-id="e03d1-147">public void setExternalContext(\[Common externalContext\])</span></span>                                                                                                                          | <span data-ttu-id="e03d1-148">dataSetRun オブジェクトの外部コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-148">Sets the external context on the dataSetRun object.</span></span>                           |
| <span data-ttu-id="e03d1-149">public void init()</span><span class="sxs-lookup"><span data-stu-id="e03d1-149">public void init()</span></span>                                                                                                                                                                  |                                                                               |
| <span data-ttu-id="e03d1-150">public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)</span><span class="sxs-lookup"><span data-stu-id="e03d1-150">public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)</span></span>                    | <span data-ttu-id="e03d1-151">階層データの参照を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-151">Enables hierarchical data browsing.</span></span>                                           |
| <span data-ttu-id="e03d1-152">public void disableHierarchicalDataBrowsing(str dataSourceName)</span><span class="sxs-lookup"><span data-stu-id="e03d1-152">public void disableHierarchicalDataBrowsing(str dataSourceName)</span></span>                                                                                                                     | <span data-ttu-id="e03d1-153">階層データの参照を無効にします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-153">Disables hierarchical data browsing.</span></span>                                          |

## <a name="method-adddatasource"></a><span data-ttu-id="e03d1-154">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-154">Method addDataSource</span></span>

<span data-ttu-id="e03d1-155">dataSetRun クラスに新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-155">Adds a new data source to the dataSetRun class.</span></span>

```xpp
public FormDataSource addDataSource(TableId tableId, [str joinDataSourceName], [DataSourceLinkTypePropertyValues linkType], [FieldId joinFieldId], [str newDataSourceName])
```

### <a name="parameters---adddatasource"></a><span data-ttu-id="e03d1-156">パラメーター - addDataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-156">Parameters - addDataSource</span></span>

<span data-ttu-id="e03d1-157">tableId</span><span class="sxs-lookup"><span data-stu-id="e03d1-157">tableId</span></span>  
<span data-ttu-id="e03d1-158">新しいデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-158">The name of the new data source.</span></span>

<!-- -->

<span data-ttu-id="e03d1-159">joinDataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-159">joinDataSourceName</span></span>  
<span data-ttu-id="e03d1-160">新しいデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-160">The name of the new data source.</span></span>

<!-- -->

<span data-ttu-id="e03d1-161">linkType</span><span class="sxs-lookup"><span data-stu-id="e03d1-161">linkType</span></span>  
<span data-ttu-id="e03d1-162">新しいデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-162">The name of the new data source.</span></span>

<!-- -->

<span data-ttu-id="e03d1-163">joinFieldId</span><span class="sxs-lookup"><span data-stu-id="e03d1-163">joinFieldId</span></span>  
<span data-ttu-id="e03d1-164">新しいデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-164">The name of the new data source.</span></span>

<!-- -->

<span data-ttu-id="e03d1-165">newDataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-165">newDataSourceName</span></span>  
<span data-ttu-id="e03d1-166">新しいデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-166">The name of the new data source.</span></span>

### <a name="return-value---adddatasource"></a><span data-ttu-id="e03d1-167">戻り値 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-167">Return Value - addDataSource</span></span>

<span data-ttu-id="e03d1-168">新しいデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-168">The new data source.</span></span>

## <a name="method-dataset"></a><span data-ttu-id="e03d1-169">メソッド dataSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-169">Method dataSet</span></span>

```xpp
public DataSet dataSet()
```

### <a name="return-value---dataset"></a><span data-ttu-id="e03d1-170">戻り値 - dataSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-170">Return Value - dataSet</span></span>

## <a name="method-datasource"></a><span data-ttu-id="e03d1-171">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-171">Method dataSource</span></span>

```xpp
public FormObjectSet dataSource([AnyType objectSet])
```

### <a name="parameters---datasource"></a><span data-ttu-id="e03d1-172">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-172">Parameters - dataSource</span></span>

<span data-ttu-id="e03d1-173">objectSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-173">objectSet</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="e03d1-174">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="e03d1-174">Return Value - dataSource</span></span>

## <a name="method-datasourcebyid"></a><span data-ttu-id="e03d1-175">メソッド dataSourceById</span><span class="sxs-lookup"><span data-stu-id="e03d1-175">Method dataSourceById</span></span>

```xpp
public FormObjectSet dataSourceById(int id)
```

### <a name="parameters---datasourcebyid"></a><span data-ttu-id="e03d1-176">パラメーター - dataSourceById</span><span class="sxs-lookup"><span data-stu-id="e03d1-176">Parameters - dataSourceById</span></span>

<span data-ttu-id="e03d1-177">id</span><span class="sxs-lookup"><span data-stu-id="e03d1-177">id</span></span>  

### <a name="return-value---datasourcebyid"></a><span data-ttu-id="e03d1-178">戻り値 - dataSourceById</span><span class="sxs-lookup"><span data-stu-id="e03d1-178">Return Value - dataSourceById</span></span>

## <a name="method-datasourcecount"></a><span data-ttu-id="e03d1-179">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="e03d1-179">Method dataSourceCount</span></span>

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a><span data-ttu-id="e03d1-180">戻り値 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="e03d1-180">Return Value - dataSourceCount</span></span>

## <a name="method-getactivefields"></a><span data-ttu-id="e03d1-181">メソッド getActiveFields</span><span class="sxs-lookup"><span data-stu-id="e03d1-181">Method getActiveFields</span></span>

```xpp
public Array getActiveFields(int dataSourceId)
```

### <a name="parameters---getactivefields"></a><span data-ttu-id="e03d1-182">パラメーター - getActiveFields</span><span class="sxs-lookup"><span data-stu-id="e03d1-182">Parameters - getActiveFields</span></span>

<span data-ttu-id="e03d1-183">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="e03d1-183">dataSourceId</span></span>  

### <a name="return-value---getactivefields"></a><span data-ttu-id="e03d1-184">戻り値 - getActiveFields</span><span class="sxs-lookup"><span data-stu-id="e03d1-184">Return Value - getActiveFields</span></span>

## <a name="method-getchildrenbyid"></a><span data-ttu-id="e03d1-185">メソッド getChildrenById</span><span class="sxs-lookup"><span data-stu-id="e03d1-185">Method getChildrenById</span></span>

<span data-ttu-id="e03d1-186">親 ID を使用してデータ ソースの子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-186">Gets the children of a data source by using the parent ID.</span></span>

```xpp
public container getChildrenById(str dataSourceName, [AnyType parentId])
```

### <a name="parameters---getchildrenbyid"></a><span data-ttu-id="e03d1-187">パラメーター - getChildrenById</span><span class="sxs-lookup"><span data-stu-id="e03d1-187">Parameters - getChildrenById</span></span>

<span data-ttu-id="e03d1-188">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-188">dataSourceName</span></span>  
<span data-ttu-id="e03d1-189">親 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-189">The parent ID.</span></span>

<!-- -->

<span data-ttu-id="e03d1-190">parentId</span><span class="sxs-lookup"><span data-stu-id="e03d1-190">parentId</span></span>  
<span data-ttu-id="e03d1-191">親 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-191">The parent ID.</span></span>

### <a name="return-value---getchildrenbyid"></a><span data-ttu-id="e03d1-192">戻り値 - getChildrenById</span><span class="sxs-lookup"><span data-stu-id="e03d1-192">Return Value - getChildrenById</span></span>

<span data-ttu-id="e03d1-193">子のためのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e03d1-193">A container for the children.</span></span>

## <a name="method-getchildrenbyindex"></a><span data-ttu-id="e03d1-194">メソッド getChildrenByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-194">Method getChildrenByIndex</span></span>

<span data-ttu-id="e03d1-195">親インデックスを使用してデータ ソースの子を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-195">Gets the children of a data source by using the parent index.</span></span>

```xpp
public container getChildrenByIndex(str dataSourceName, [int parentIndex])
```

### <a name="parameters---getchildrenbyindex"></a><span data-ttu-id="e03d1-196">パラメーター - getChildrenByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-196">Parameters - getChildrenByIndex</span></span>

<span data-ttu-id="e03d1-197">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-197">dataSourceName</span></span>  
<span data-ttu-id="e03d1-198">親インデックス。</span><span class="sxs-lookup"><span data-stu-id="e03d1-198">The parent index.</span></span>

<!-- -->

<span data-ttu-id="e03d1-199">parentIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-199">parentIndex</span></span>  
<span data-ttu-id="e03d1-200">親インデックス。</span><span class="sxs-lookup"><span data-stu-id="e03d1-200">The parent index.</span></span>

### <a name="return-value---getchildrenbyindex"></a><span data-ttu-id="e03d1-201">戻り値 - getChildrenByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-201">Return Value - getChildrenByIndex</span></span>

<span data-ttu-id="e03d1-202">子のためのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e03d1-202">A container for the children.</span></span>

## <a name="method-getlasterror"></a><span data-ttu-id="e03d1-203">メソッド getLastError</span><span class="sxs-lookup"><span data-stu-id="e03d1-203">Method getLastError</span></span>

```xpp
public DataSetError getLastError()
```

### <a name="return-value---getlasterror"></a><span data-ttu-id="e03d1-204">戻り値 - getLastError</span><span class="sxs-lookup"><span data-stu-id="e03d1-204">Return Value - getLastError</span></span>

## <a name="method-getparentbyid"></a><span data-ttu-id="e03d1-205">メソッド getParentById</span><span class="sxs-lookup"><span data-stu-id="e03d1-205">Method getParentById</span></span>

<span data-ttu-id="e03d1-206">子 ID を使用してデータ ソースの親を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-206">Gets the parent of a data source by using the child ID.</span></span>

```xpp
public AnyType getParentById(str dataSourceName, AnyType childId)
```

### <a name="parameters---getparentbyid"></a><span data-ttu-id="e03d1-207">パラメーター - getParentById</span><span class="sxs-lookup"><span data-stu-id="e03d1-207">Parameters - getParentById</span></span>

<span data-ttu-id="e03d1-208">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-208">dataSourceName</span></span>  
<span data-ttu-id="e03d1-209">子 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-209">The child ID.</span></span>

<!-- -->

<span data-ttu-id="e03d1-210">childId</span><span class="sxs-lookup"><span data-stu-id="e03d1-210">childId</span></span>  
<span data-ttu-id="e03d1-211">子 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-211">The child ID.</span></span>

### <a name="return-value---getparentbyid"></a><span data-ttu-id="e03d1-212">戻り値 - getParentById</span><span class="sxs-lookup"><span data-stu-id="e03d1-212">Return Value - getParentById</span></span>

<span data-ttu-id="e03d1-213">親 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-213">The parent ID.</span></span>

## <a name="method-getparentbyindex"></a><span data-ttu-id="e03d1-214">メソッド getParentByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-214">Method getParentByIndex</span></span>

<span data-ttu-id="e03d1-215">子インデックスを使用してデータ ソースの親を取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-215">Gets the parent of a data source by using the child index.</span></span>

```xpp
public int getParentByIndex(str dataSourceName, int childIndex)
```

### <a name="parameters---getparentbyindex"></a><span data-ttu-id="e03d1-216">パラメーター - getParentByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-216">Parameters - getParentByIndex</span></span>

<span data-ttu-id="e03d1-217">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-217">dataSourceName</span></span>  
<span data-ttu-id="e03d1-218">子インデックス。</span><span class="sxs-lookup"><span data-stu-id="e03d1-218">The child index.</span></span>

<!-- -->

<span data-ttu-id="e03d1-219">childIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-219">childIndex</span></span>  
<span data-ttu-id="e03d1-220">子インデックス。</span><span class="sxs-lookup"><span data-stu-id="e03d1-220">The child index.</span></span>

### <a name="return-value---getparentbyindex"></a><span data-ttu-id="e03d1-221">戻り値 - getParentByIndex</span><span class="sxs-lookup"><span data-stu-id="e03d1-221">Return Value - getParentByIndex</span></span>

<span data-ttu-id="e03d1-222">親 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-222">The parent ID.</span></span>

## <a name="method-getrowindexfromrowhierarchyid"></a><span data-ttu-id="e03d1-223">メソッド getRowIndexFromRowHierarchyId</span><span class="sxs-lookup"><span data-stu-id="e03d1-223">Method getRowIndexFromRowHierarchyId</span></span>

<span data-ttu-id="e03d1-224">行階層 ID を使用してデータ ソース内の行インデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-224">Gets the row index on a data source by using a row hierarchy ID.</span></span>

```xpp
public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)
```

### <a name="parameters---getrowindexfromrowhierarchyid"></a><span data-ttu-id="e03d1-225">パラメーター - getRowIndexFromRowHierarchyId</span><span class="sxs-lookup"><span data-stu-id="e03d1-225">Parameters - getRowIndexFromRowHierarchyId</span></span>

<span data-ttu-id="e03d1-226">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-226">dataSourceName</span></span>  
<span data-ttu-id="e03d1-227">行の階層 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-227">The row hierarchy ID.</span></span>

<!-- -->

<span data-ttu-id="e03d1-228">id</span><span class="sxs-lookup"><span data-stu-id="e03d1-228">id</span></span>  
<span data-ttu-id="e03d1-229">行の階層 ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-229">The row hierarchy ID.</span></span>

### <a name="return-value---getrowindexfromrowhierarchyid"></a><span data-ttu-id="e03d1-230">戻り値 - getRowIndexFromRowHierarchyId</span><span class="sxs-lookup"><span data-stu-id="e03d1-230">Return Value - getRowIndexFromRowHierarchyId</span></span>

<span data-ttu-id="e03d1-231">行インデックス。</span><span class="sxs-lookup"><span data-stu-id="e03d1-231">The row index.</span></span>

## <a name="method-initcomplete"></a><span data-ttu-id="e03d1-232">メソッド initComplete</span><span class="sxs-lookup"><span data-stu-id="e03d1-232">Method initComplete</span></span>

```xpp
public boolean initComplete()
```

### <a name="return-value---initcomplete"></a><span data-ttu-id="e03d1-233">戻り値 - initComplete</span><span class="sxs-lookup"><span data-stu-id="e03d1-233">Return Value - initComplete</span></span>

## <a name="method-name"></a><span data-ttu-id="e03d1-234">メソッド名</span><span class="sxs-lookup"><span data-stu-id="e03d1-234">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="e03d1-235">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="e03d1-235">Return Value - name</span></span>

## <a name="method-objectset"></a><span data-ttu-id="e03d1-236">メソッド objectSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-236">Method objectSet</span></span>

```xpp
public FormObjectSet objectSet([AnyType objectSet])
```

### <a name="parameters---objectset"></a><span data-ttu-id="e03d1-237">パラメーター - objectSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-237">Parameters - objectSet</span></span>

<span data-ttu-id="e03d1-238">objectSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-238">objectSet</span></span>  

### <a name="return-value---objectset"></a><span data-ttu-id="e03d1-239">戻り値 - objectSet</span><span class="sxs-lookup"><span data-stu-id="e03d1-239">Return Value - objectSet</span></span>

## <a name="method-pack"></a><span data-ttu-id="e03d1-240">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="e03d1-240">Method pack</span></span>

<span data-ttu-id="e03d1-241">DataSetRun クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-241">Serializes the current instance of the DataSetRun class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="e03d1-242">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="e03d1-242">Return Value - pack</span></span>

<span data-ttu-id="e03d1-243">DataSetRun クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e03d1-243">A container that contains the current instance of the DataSetRun class.</span></span>

## <a name="method-runcalled"></a><span data-ttu-id="e03d1-244">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="e03d1-244">Method runCalled</span></span>

```xpp
public boolean runCalled()
```

### <a name="return-value---runcalled"></a><span data-ttu-id="e03d1-245">戻り値 - runCalled</span><span class="sxs-lookup"><span data-stu-id="e03d1-245">Return Value - runCalled</span></span>

## <a name="method-unpack"></a><span data-ttu-id="e03d1-246">メソッド unpack</span><span class="sxs-lookup"><span data-stu-id="e03d1-246">Method unpack</span></span>

<span data-ttu-id="e03d1-247">pack パラメーター値を DataSetRun クラスのインスタンスに逆シリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-247">Deserializes the pack parameter value to an instance of the DataSetRun class.</span></span>

```xpp
public boolean unpack(container pack)
```

### <a name="parameters---unpack"></a><span data-ttu-id="e03d1-248">パラメーター - unpack</span><span class="sxs-lookup"><span data-stu-id="e03d1-248">Parameters - unpack</span></span>

<span data-ttu-id="e03d1-249">梱包</span><span class="sxs-lookup"><span data-stu-id="e03d1-249">pack</span></span>  
<span data-ttu-id="e03d1-250">インスタンスを逆シリアル化するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="e03d1-250">The container from which to deserialize the instance.</span></span>

### <a name="return-value---unpack"></a><span data-ttu-id="e03d1-251">戻り値 - unpack</span><span class="sxs-lookup"><span data-stu-id="e03d1-251">Return Value - unpack</span></span>

<span data-ttu-id="e03d1-252">逆シリアル化が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e03d1-252">true if deserialization was successful; otherwise, false.</span></span>

## <a name="method-create"></a><span data-ttu-id="e03d1-253">メソッド create</span><span class="sxs-lookup"><span data-stu-id="e03d1-253">Method create</span></span>

```xpp
public static DataSetRun create(str name, container pack)
```

### <a name="parameters---create"></a><span data-ttu-id="e03d1-254">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="e03d1-254">Parameters - create</span></span>

<span data-ttu-id="e03d1-255">名前</span><span class="sxs-lookup"><span data-stu-id="e03d1-255">name</span></span>  

<!-- -->

<span data-ttu-id="e03d1-256">梱包</span><span class="sxs-lookup"><span data-stu-id="e03d1-256">pack</span></span>  

### <a name="return-value---create"></a><span data-ttu-id="e03d1-257">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="e03d1-257">Return Value - create</span></span>

## <a name="method-createruntime"></a><span data-ttu-id="e03d1-258">メソッド createRunTime</span><span class="sxs-lookup"><span data-stu-id="e03d1-258">Method createRunTime</span></span>

```xpp
public static DataSetRun createRunTime(container pack)
```

### <a name="parameters---createruntime"></a><span data-ttu-id="e03d1-259">パラメーター - createRunTime</span><span class="sxs-lookup"><span data-stu-id="e03d1-259">Parameters - createRunTime</span></span>

<span data-ttu-id="e03d1-260">梱包</span><span class="sxs-lookup"><span data-stu-id="e03d1-260">pack</span></span>  

### <a name="return-value---createruntime"></a><span data-ttu-id="e03d1-261">戻り値 - createRunTime</span><span class="sxs-lookup"><span data-stu-id="e03d1-261">Return Value - createRunTime</span></span>

## <a name="method-setlasterror"></a><span data-ttu-id="e03d1-262">メソッド setLastError</span><span class="sxs-lookup"><span data-stu-id="e03d1-262">Method setLastError</span></span>

```xpp
public void setLastError(DataSetError error)
```

### <a name="parameters---setlasterror"></a><span data-ttu-id="e03d1-263">パラメーター - setLastError</span><span class="sxs-lookup"><span data-stu-id="e03d1-263">Parameters - setLastError</span></span>

<span data-ttu-id="e03d1-264">エラー</span><span class="sxs-lookup"><span data-stu-id="e03d1-264">error</span></span>  

## <a name="method-run"></a><span data-ttu-id="e03d1-265">メソッド run</span><span class="sxs-lookup"><span data-stu-id="e03d1-265">Method run</span></span>

```xpp
public void run()
```

## <a name="method-setlookupmode"></a><span data-ttu-id="e03d1-266">メソッド setLookupMode</span><span class="sxs-lookup"><span data-stu-id="e03d1-266">Method setLookupMode</span></span>

<span data-ttu-id="e03d1-267">データセットをルックアップ モードにします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-267">Puts the dataset into lookup mode.</span></span>

```xpp
public void setLookupMode()
```

## <a name="method-new"></a><span data-ttu-id="e03d1-268">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e03d1-268">Method new</span></span>

<span data-ttu-id="e03d1-269">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-269">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(xArgs args)
```

### <a name="parameters---new"></a><span data-ttu-id="e03d1-270">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e03d1-270">Parameters - new</span></span>

<span data-ttu-id="e03d1-271">args</span><span class="sxs-lookup"><span data-stu-id="e03d1-271">args</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="e03d1-272">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="e03d1-272">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-createrecord"></a><span data-ttu-id="e03d1-273">メソッド createRecord</span><span class="sxs-lookup"><span data-stu-id="e03d1-273">Method createRecord</span></span>

<span data-ttu-id="e03d1-274">新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-274">Creates a new record.</span></span>

```xpp
public void createRecord(str formDataSourceName, [boolean append])
```

### <a name="parameters---createrecord"></a><span data-ttu-id="e03d1-275">パラメーター - createRecord</span><span class="sxs-lookup"><span data-stu-id="e03d1-275">Parameters - createRecord</span></span>

<span data-ttu-id="e03d1-276">formDataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-276">formDataSourceName</span></span>  
<span data-ttu-id="e03d1-277">追加するレコード。</span><span class="sxs-lookup"><span data-stu-id="e03d1-277">The record to append.</span></span>

<!-- -->

<span data-ttu-id="e03d1-278">append</span><span class="sxs-lookup"><span data-stu-id="e03d1-278">append</span></span>  
<span data-ttu-id="e03d1-279">追加するレコード。</span><span class="sxs-lookup"><span data-stu-id="e03d1-279">The record to append.</span></span>

## <a name="method-setactivefields"></a><span data-ttu-id="e03d1-280">メソッド setActiveFields</span><span class="sxs-lookup"><span data-stu-id="e03d1-280">Method setActiveFields</span></span>

```xpp
public void setActiveFields(int dataSourceId, Array fieldIds)
```

### <a name="parameters---setactivefields"></a><span data-ttu-id="e03d1-281">パラメーター - setActiveFields</span><span class="sxs-lookup"><span data-stu-id="e03d1-281">Parameters - setActiveFields</span></span>

<span data-ttu-id="e03d1-282">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="e03d1-282">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="e03d1-283">fieldIds</span><span class="sxs-lookup"><span data-stu-id="e03d1-283">fieldIds</span></span>  

## <a name="method-setexternalcontext"></a><span data-ttu-id="e03d1-284">メソッド setExternalContext</span><span class="sxs-lookup"><span data-stu-id="e03d1-284">Method setExternalContext</span></span>

<span data-ttu-id="e03d1-285">dataSetRun オブジェクトの外部コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="e03d1-285">Sets the external context on the dataSetRun object.</span></span>

```xpp
public void setExternalContext([Common externalContext])
```

### <a name="parameters---setexternalcontext"></a><span data-ttu-id="e03d1-286">パラメーター - setExternalContext</span><span class="sxs-lookup"><span data-stu-id="e03d1-286">Parameters - setExternalContext</span></span>

<span data-ttu-id="e03d1-287">externalContext</span><span class="sxs-lookup"><span data-stu-id="e03d1-287">externalContext</span></span>  
<span data-ttu-id="e03d1-288">外部コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="e03d1-288">The external context.</span></span>

## <a name="method-init"></a><span data-ttu-id="e03d1-289">メソッド init</span><span class="sxs-lookup"><span data-stu-id="e03d1-289">Method init</span></span>

```xpp
public void init()
```

## <a name="method-enablehierarchicaldatabrowsing"></a><span data-ttu-id="e03d1-290">メソッド enableHierarchicalDataBrowsing</span><span class="sxs-lookup"><span data-stu-id="e03d1-290">Method enableHierarchicalDataBrowsing</span></span>

<span data-ttu-id="e03d1-291">階層データの参照を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-291">Enables hierarchical data browsing.</span></span>

```xpp
public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)
```

### <a name="parameters---enablehierarchicaldatabrowsing"></a><span data-ttu-id="e03d1-292">パラメーター - enableHierarchicalDataBrowsing</span><span class="sxs-lookup"><span data-stu-id="e03d1-292">Parameters - enableHierarchicalDataBrowsing</span></span>

<span data-ttu-id="e03d1-293">hierarchyPKDataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-293">hierarchyPKDataSourceName</span></span>  
<span data-ttu-id="e03d1-294">階層内の外部キー フィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-294">The ID of the foreign key field in the hierarchy.</span></span>

<!-- -->

<span data-ttu-id="e03d1-295">hierarchyPKfieldId</span><span class="sxs-lookup"><span data-stu-id="e03d1-295">hierarchyPKfieldId</span></span>  
<span data-ttu-id="e03d1-296">階層内の外部キー フィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-296">The ID of the foreign key field in the hierarchy.</span></span>

<!-- -->

<span data-ttu-id="e03d1-297">hierarchyFKDataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-297">hierarchyFKDataSourceName</span></span>  
<span data-ttu-id="e03d1-298">階層内の外部キー フィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-298">The ID of the foreign key field in the hierarchy.</span></span>

<!-- -->

<span data-ttu-id="e03d1-299">hierarchyFKfieldId</span><span class="sxs-lookup"><span data-stu-id="e03d1-299">hierarchyFKfieldId</span></span>  
<span data-ttu-id="e03d1-300">階層内の外部キー フィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="e03d1-300">The ID of the foreign key field in the hierarchy.</span></span>

## <a name="method-disablehierarchicaldatabrowsing"></a><span data-ttu-id="e03d1-301">メソッド disableHierarchicalDataBrowsing</span><span class="sxs-lookup"><span data-stu-id="e03d1-301">Method disableHierarchicalDataBrowsing</span></span>

<span data-ttu-id="e03d1-302">階層データの参照を無効にします。</span><span class="sxs-lookup"><span data-stu-id="e03d1-302">Disables hierarchical data browsing.</span></span>

```xpp
public void disableHierarchicalDataBrowsing(str dataSourceName)
```

### <a name="parameters---disablehierarchicaldatabrowsing"></a><span data-ttu-id="e03d1-303">パラメーター - disableHierarchicalDataBrowsing</span><span class="sxs-lookup"><span data-stu-id="e03d1-303">Parameters - disableHierarchicalDataBrowsing</span></span>

<span data-ttu-id="e03d1-304">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="e03d1-304">dataSourceName</span></span>  
<span data-ttu-id="e03d1-305">階層データの参照を無効にするデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="e03d1-305">The name of the data source to disable hierarchical data browsing on.</span></span>

