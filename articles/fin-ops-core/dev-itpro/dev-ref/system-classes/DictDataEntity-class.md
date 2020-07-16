---
title: DictDataEntity クラス
description: このトピックでは、DictDataEntity クラスについて説明します。
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
ms.openlocfilehash: b69788ad9349ee2ea8d00dfe2e34b9f93fbfab06
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502991"
---
# <a name="class-dictdataentity"></a><span data-ttu-id="76b42-103">クラス DictDataEntity</span><span class="sxs-lookup"><span data-stu-id="76b42-103">Class DictDataEntity</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictDataEntity extends DictView
```

## <a name="remarks"></a><span data-ttu-id="76b42-104">備考</span><span class="sxs-lookup"><span data-stu-id="76b42-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="76b42-105">例</span><span class="sxs-lookup"><span data-stu-id="76b42-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="76b42-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="76b42-106">Methods</span></span>

| <span data-ttu-id="76b42-107">方法</span><span class="sxs-lookup"><span data-stu-id="76b42-107">Method</span></span>                                                  | <span data-ttu-id="76b42-108">説明</span><span class="sxs-lookup"><span data-stu-id="76b42-108">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="76b42-109">public boolean isAggregateDataEntity()</span><span class="sxs-lookup"><span data-stu-id="76b42-109">public boolean isAggregateDataEntity()</span></span>                  |             |
| <span data-ttu-id="76b42-110">public boolean isReadOnly()</span><span class="sxs-lookup"><span data-stu-id="76b42-110">public boolean isReadOnly()</span></span>                             |             |
| <span data-ttu-id="76b42-111">public str primaryCompanyContext()</span><span class="sxs-lookup"><span data-stu-id="76b42-111">public str primaryCompanyContext()</span></span>                      |             |
| <span data-ttu-id="76b42-112">public str primaryKey()</span><span class="sxs-lookup"><span data-stu-id="76b42-112">public str primaryKey()</span></span>                                 |             |
| <span data-ttu-id="76b42-113">public boolean supportsSetBasedSqlOperations()</span><span class="sxs-lookup"><span data-stu-id="76b42-113">public boolean supportsSetBasedSqlOperations()</span></span>          |             |
| <span data-ttu-id="76b42-114">public AutoNo enableSetBasedSqlOperations()</span><span class="sxs-lookup"><span data-stu-id="76b42-114">public AutoNo enableSetBasedSqlOperations()</span></span>             |             |
| <span data-ttu-id="76b42-115">public str modules()</span><span class="sxs-lookup"><span data-stu-id="76b42-115">public str modules()</span></span>                                    |             |
| <span data-ttu-id="76b42-116">public EntityCategory entityCategory()</span><span class="sxs-lookup"><span data-stu-id="76b42-116">public EntityCategory entityCategory()</span></span>                  |             |
| <span data-ttu-id="76b42-117">public boolean dataManagementEnabled()</span><span class="sxs-lookup"><span data-stu-id="76b42-117">public boolean dataManagementEnabled()</span></span>                  |             |
| <span data-ttu-id="76b42-118">public str dataManagementStagingTable()</span><span class="sxs-lookup"><span data-stu-id="76b42-118">public str dataManagementStagingTable()</span></span>                 |             |
| <span data-ttu-id="76b42-119">public str publicCollectionName()</span><span class="sxs-lookup"><span data-stu-id="76b42-119">public str publicCollectionName()</span></span>                       |             |
| <span data-ttu-id="76b42-120">public str publicEntityName()</span><span class="sxs-lookup"><span data-stu-id="76b42-120">public str publicEntityName()</span></span>                           |             |
| <span data-ttu-id="76b42-121">public boolean dataSourceIsReadOnly(str dataSourceName)</span><span class="sxs-lookup"><span data-stu-id="76b42-121">public boolean dataSourceIsReadOnly(str dataSourceName)</span></span> |             |
| <span data-ttu-id="76b42-122">public str dataSourceID2Name(int dataSourceId)</span><span class="sxs-lookup"><span data-stu-id="76b42-122">public str dataSourceID2Name(int dataSourceId)</span></span>          |             |
| <span data-ttu-id="76b42-123">public boolean hasExtensionFields()</span><span class="sxs-lookup"><span data-stu-id="76b42-123">public boolean hasExtensionFields()</span></span>                     |             |
| <span data-ttu-id="76b42-124">public List getExtensionFieldNames()</span><span class="sxs-lookup"><span data-stu-id="76b42-124">public List getExtensionFieldNames()</span></span>                    |             |
| <span data-ttu-id="76b42-125">::public static List listOfDataEntities()</span><span class="sxs-lookup"><span data-stu-id="76b42-125">::public static List listOfDataEntities()</span></span>               |             |
| <span data-ttu-id="76b42-126">public void new(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="76b42-126">public void new(TableId tableId)</span></span>                        |             |

## <a name="method-isaggregatedataentity"></a><span data-ttu-id="76b42-127">メソッド isAggregateDataEntity</span><span class="sxs-lookup"><span data-stu-id="76b42-127">Method isAggregateDataEntity</span></span>

```xpp
public boolean isAggregateDataEntity()
```

### <a name="return-value---isaggregatedataentity"></a><span data-ttu-id="76b42-128">戻り値 - isAggregateDataEntity</span><span class="sxs-lookup"><span data-stu-id="76b42-128">Return Value - isAggregateDataEntity</span></span>

## <a name="method-isreadonly"></a><span data-ttu-id="76b42-129">メソッド isReadOnly</span><span class="sxs-lookup"><span data-stu-id="76b42-129">Method isReadOnly</span></span>

```xpp
public boolean isReadOnly()
```

### <a name="return-value---isreadonly"></a><span data-ttu-id="76b42-130">戻り値 - DictDataEntity</span><span class="sxs-lookup"><span data-stu-id="76b42-130">Return Value - isReadOnly</span></span>

## <a name="method-primarycompanycontext"></a><span data-ttu-id="76b42-131">メソッド primaryCompanyContext</span><span class="sxs-lookup"><span data-stu-id="76b42-131">Method primaryCompanyContext</span></span>

```xpp
public str primaryCompanyContext()
```

### <a name="return-value---primarycompanycontext"></a><span data-ttu-id="76b42-132">戻り値 - primaryCompanyContext</span><span class="sxs-lookup"><span data-stu-id="76b42-132">Return Value - primaryCompanyContext</span></span>

## <a name="method-primarykey"></a><span data-ttu-id="76b42-133">メソッド primaryKey</span><span class="sxs-lookup"><span data-stu-id="76b42-133">Method primaryKey</span></span>

```xpp
public str primaryKey()
```

### <a name="return-value---primarykey"></a><span data-ttu-id="76b42-134">戻り値 - primaryKey</span><span class="sxs-lookup"><span data-stu-id="76b42-134">Return Value - primaryKey</span></span>

## <a name="method-supportssetbasedsqloperations"></a><span data-ttu-id="76b42-135">メソッド supportsSetBasedSqlOperations</span><span class="sxs-lookup"><span data-stu-id="76b42-135">Method supportsSetBasedSqlOperations</span></span>

```xpp
public boolean supportsSetBasedSqlOperations()
```

### <a name="return-value---supportssetbasedsqloperations"></a><span data-ttu-id="76b42-136">戻り値 - supportsSetBasedSqlOperations</span><span class="sxs-lookup"><span data-stu-id="76b42-136">Return Value - supportsSetBasedSqlOperations</span></span>

## <a name="method-enablesetbasedsqloperations"></a><span data-ttu-id="76b42-137">メソッド enableSetBasedSqlOperations</span><span class="sxs-lookup"><span data-stu-id="76b42-137">Method enableSetBasedSqlOperations</span></span>

```xpp
public AutoNo enableSetBasedSqlOperations()
```

### <a name="return-value---enablesetbasedsqloperations"></a><span data-ttu-id="76b42-138">戻り値 - enableSetBasedSqlOperations</span><span class="sxs-lookup"><span data-stu-id="76b42-138">Return Value - enableSetBasedSqlOperations</span></span>

## <a name="method-modules"></a><span data-ttu-id="76b42-139">メソッド modules</span><span class="sxs-lookup"><span data-stu-id="76b42-139">Method modules</span></span>

```xpp
public str modules()
```

### <a name="return-value---modules"></a><span data-ttu-id="76b42-140">戻り値 - modules</span><span class="sxs-lookup"><span data-stu-id="76b42-140">Return Value - modules</span></span>

## <a name="method-entitycategory"></a><span data-ttu-id="76b42-141">メソッド entityCategory</span><span class="sxs-lookup"><span data-stu-id="76b42-141">Method entityCategory</span></span>

```xpp
public EntityCategory entityCategory()
```

### <a name="return-value---entitycategory"></a><span data-ttu-id="76b42-142">戻り値 - entityCategory</span><span class="sxs-lookup"><span data-stu-id="76b42-142">Return Value - entityCategory</span></span>

## <a name="method-datamanagementenabled"></a><span data-ttu-id="76b42-143">メソッド dataManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="76b42-143">Method dataManagementEnabled</span></span>

```xpp
public boolean dataManagementEnabled()
```

### <a name="return-value---datamanagementenabled"></a><span data-ttu-id="76b42-144">戻り値 - dataManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="76b42-144">Return Value - dataManagementEnabled</span></span>

## <a name="method-datamanagementstagingtable"></a><span data-ttu-id="76b42-145">メソッド dataManagementStagingTable</span><span class="sxs-lookup"><span data-stu-id="76b42-145">Method dataManagementStagingTable</span></span>

```xpp
public str dataManagementStagingTable()
```

### <a name="return-value---datamanagementstagingtable"></a><span data-ttu-id="76b42-146">戻り値 - dataManagementStagingTable</span><span class="sxs-lookup"><span data-stu-id="76b42-146">Return Value - dataManagementStagingTable</span></span>

## <a name="method-publiccollectionname"></a><span data-ttu-id="76b42-147">メソッド publicCollectionName</span><span class="sxs-lookup"><span data-stu-id="76b42-147">Method publicCollectionName</span></span>

```xpp
public str publicCollectionName()
```

### <a name="return-value---publiccollectionname"></a><span data-ttu-id="76b42-148">戻り値 - publicCollectionName</span><span class="sxs-lookup"><span data-stu-id="76b42-148">Return Value - publicCollectionName</span></span>

## <a name="method-publicentityname"></a><span data-ttu-id="76b42-149">メソッド publicEntityName</span><span class="sxs-lookup"><span data-stu-id="76b42-149">Method publicEntityName</span></span>

```xpp
public str publicEntityName()
```

### <a name="return-value---publicentityname"></a><span data-ttu-id="76b42-150">戻り値 - publicEntityName</span><span class="sxs-lookup"><span data-stu-id="76b42-150">Return Value - publicEntityName</span></span>

## <a name="method-datasourceisreadonly"></a><span data-ttu-id="76b42-151">メソッド dataSourceIsReadOnly</span><span class="sxs-lookup"><span data-stu-id="76b42-151">Method dataSourceIsReadOnly</span></span>

```xpp
public boolean dataSourceIsReadOnly(str dataSourceName)
```

### <a name="parameters---datasourceisreadonly"></a><span data-ttu-id="76b42-152">パラメーター - dataSourceIsReadOnly</span><span class="sxs-lookup"><span data-stu-id="76b42-152">Parameters - dataSourceIsReadOnly</span></span>

<span data-ttu-id="76b42-153">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="76b42-153">dataSourceName</span></span>  

### <a name="return-value---datasourceisreadonly"></a><span data-ttu-id="76b42-154">戻り値 - dataSourceIsReadOnly</span><span class="sxs-lookup"><span data-stu-id="76b42-154">Return Value - dataSourceIsReadOnly</span></span>

## <a name="method-datasourceid2name"></a><span data-ttu-id="76b42-155">メソッド dataSourceID2Name</span><span class="sxs-lookup"><span data-stu-id="76b42-155">Method dataSourceID2Name</span></span>

```xpp
public str dataSourceID2Name(int dataSourceId)
```

### <a name="parameters---datasourceid2name"></a><span data-ttu-id="76b42-156">パラメーター - dataSourceID2Name</span><span class="sxs-lookup"><span data-stu-id="76b42-156">Parameters - dataSourceID2Name</span></span>

<span data-ttu-id="76b42-157">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="76b42-157">dataSourceId</span></span>  

### <a name="return-value---datasourceid2name"></a><span data-ttu-id="76b42-158">戻り値 - dataSourceID2Name</span><span class="sxs-lookup"><span data-stu-id="76b42-158">Return Value - dataSourceID2Name</span></span>

## <a name="method-hasextensionfields"></a><span data-ttu-id="76b42-159">メソッド hasExtensionFields</span><span class="sxs-lookup"><span data-stu-id="76b42-159">Method hasExtensionFields</span></span>

```xpp
public boolean hasExtensionFields()
```

### <a name="return-value---hasextensionfields"></a><span data-ttu-id="76b42-160">戻り値 - hasExtensionFields</span><span class="sxs-lookup"><span data-stu-id="76b42-160">Return Value - hasExtensionFields</span></span>

## <a name="method-getextensionfieldnames"></a><span data-ttu-id="76b42-161">メソッド getExtensionFieldNames</span><span class="sxs-lookup"><span data-stu-id="76b42-161">Method getExtensionFieldNames</span></span>

```xpp
public List getExtensionFieldNames()
```

### <a name="return-value---getextensionfieldnames"></a><span data-ttu-id="76b42-162">戻り値 - getExtensionFieldNames</span><span class="sxs-lookup"><span data-stu-id="76b42-162">Return Value - getExtensionFieldNames</span></span>

## <a name="method-listofdataentities"></a><span data-ttu-id="76b42-163">メソッド listOfDataEntities</span><span class="sxs-lookup"><span data-stu-id="76b42-163">Method listOfDataEntities</span></span>

```xpp
public static List listOfDataEntities()
```

### <a name="return-value---listofdataentities"></a><span data-ttu-id="76b42-164">戻り値 - listOfDataEntities</span><span class="sxs-lookup"><span data-stu-id="76b42-164">Return Value - listOfDataEntities</span></span>

## <a name="method-new"></a><span data-ttu-id="76b42-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="76b42-165">Method new</span></span>

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a><span data-ttu-id="76b42-166">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="76b42-166">Parameters - new</span></span>

<span data-ttu-id="76b42-167">tableId</span><span class="sxs-lookup"><span data-stu-id="76b42-167">tableId</span></span>  

